# LaTex教程

## 基础配置(vscode+sumatraPDF外部)

```json
{
    //------------------------------LaTeX 配置----------------------------------
       // 设置是否自动编译
       "latex-workshop.latex.autoBuild.run":"never",
       //右键菜单
       "latex-workshop.showContextMenu":true,
       //从使用的包中自动补全命令和环境
       "latex-workshop.intellisense.package.enabled": true,
       //编译出错时设置是否弹出气泡设置
       "latex-workshop.message.error.show": false,
       "latex-workshop.message.warning.show": false,
       // 编译工具和命令
       "latex-workshop.latex.tools": [
           {
               "name": "xelatex",
               "command": "xelatex",
               "args": [
                   "-synctex=1",
                   "-interaction=nonstopmode",
                   "-file-line-error",
                   "%DOCFILE%"
               ]
           },
           {
               "name": "pdflatex",
               "command": "pdflatex",
               "args": [
                   "-synctex=1",
                   "-interaction=nonstopmode",
                   "-file-line-error",
                   "%DOCFILE%"
               ]
           },
           {
               "name": "latexmk",
               "command": "latexmk",
               "args": [
                   "-synctex=1",
                   "-interaction=nonstopmode",
                   "-file-line-error",
                   "-pdf",
                   "-outdir=%OUTDIR%",
                   "%DOCFILE%"
               ]
           },
           {
               "name": "bibtex",
               "command": "bibtex",
               "args": [
                   "%DOCFILE%"
               ]
           }
       ],
       // 用于配置编译链
       "latex-workshop.latex.recipes": [
           {
               "name": "XeLaTeX",
               "tools": [
                   "xelatex"
               ]
           },
           {
               "name": "PDFLaTeX",
               "tools": [
                   "pdflatex"
               ]
           },
           {
               "name": "BibTeX",
               "tools": [
                   "bibtex"
               ]
           },
           {
               "name": "LaTeXmk",
               "tools": [
                   "latexmk"
               ]
           },
           {
               "name": "xelatex -> bibtex -> xelatex*2",
               "tools": [
                   "xelatex",
                   "bibtex",
                   "xelatex",
                   "xelatex"
               ]
           },
           {
               "name": "pdflatex -> bibtex -> pdflatex*2",
               "tools": [
                   "pdflatex",
                   "bibtex",
                   "pdflatex",
                   "pdflatex"
               ]
           }
       ],
       //文件清理。此属性必须是字符串数组
       "latex-workshop.latex.clean.fileTypes": [
           "*.aux",
           "*.bbl",
           "*.blg",
           "*.idx",
           "*.ind",
           "*.lof",
           "*.lot",
           "*.out",
           "*.toc",
           "*.acn",
           "*.acr",
           "*.alg",
           "*.glg",
           "*.glo",
           "*.gls",
           "*.ist",
           "*.fls",
           "*.log",
           "*.fdb_latexmk"
       ],
       //设置为onFaild 在构建失败后清除辅助文件
       "latex-workshop.latex.autoClean.run": "onFailed",
       // 使用上次的recipe编译组合
       "latex-workshop.latex.recipe.default": "lastUsed",
       // 用于反向同步的内部查看器的键绑定。ctrl/cmd +点击(默认)或双击
    "latex-workshop.view.pdf.internal.synctex.keybinding": "double-click",
       // 使用外部查看器时要执行的命令。此功能不受官方支持。
    "latex-workshop.view.pdf.viewer": "external",

    "latex-workshop.view.pdf.external.viewer.command": "C:\\Users\\sunho\\AppData\\Local\\SumatraPDF\\SumatraPDF.exe",
    "latex-workshop.view.pdf.external.viewer.args": [
            "-forward-search",
            "%TEX%",
            "%LINE%",
            "-reuse-instance",
            "%PDF%"
    ], 

    "latex-workshop.view.pdf.external.synctex.command": "C:\\Users\\sunho\\AppData\\Local\\SumatraPDF\\SumatraPDF.exe",
    "latex-workshop.view.pdf.external.synctex.args": [
            "-forward-search",
            "%TEX%",
            "%LINE%",
            "-reuse-instance",
            "%PDF%"
    ]
   }
```

```bash
sumatraPDF 配置--选项--命令

"C:\Users\roger\AppData\Local\Programs\Microsoft VS Code\Code.exe" "C:\Users\roger\AppData\Local\Programs\Microsoft VS Code\resources\app\out\cli.js" --ms-enable-electron-run-as-node -r -g "%f:%l"
```

## 基础配置(vscode+内部pdf)

```json
{
    "latex-workshop.latex.autoBuild.run": "never",
    "latex-workshop.showContextMenu": true,
    "latex-workshop.intellisense.package.enabled": true,
    "latex-workshop.message.error.show": false,
    "latex-workshop.message.warning.show": false,
    "latex-workshop.latex.tools": [
        {
            "name": "xelatex",
            "command": "xelatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOCFILE%"
            ]
        },
        {
            "name": "pdflatex",
            "command": "pdflatex",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "%DOCFILE%"
            ]
        },
        {
            "name": "latexmk",
            "command": "latexmk",
            "args": [
                "-synctex=1",
                "-interaction=nonstopmode",
                "-file-line-error",
                "-pdf",
                "-outdir=%OUTDIR%",
                "%DOCFILE%"
            ]
        },
        {
            "name": "bibtex",
            "command": "bibtex",
            "args": [
                "%DOCFILE%"
            ]
        }
    ],
    "latex-workshop.latex.recipes": [
        {
            "name": "XeLaTeX",
            "tools": [
                "xelatex"
            ]
        },
        {
            "name": "PDFLaTeX",
            "tools": [
                "pdflatex"
            ]
        },
        {
            "name": "BibTeX",
            "tools": [
                "bibtex"
            ]
        },
        {
            "name": "LaTeXmk",
            "tools": [
                "latexmk"
            ]
        },
        {
            "name": "xelatex -> bibtex -> xelatex*2",
            "tools": [
                "xelatex",
                "bibtex",
                "xelatex",
                "xelatex"
            ]
        },
        {
            "name": "pdflatex -> bibtex -> pdflatex*2",
            "tools": [
                "pdflatex",
                "bibtex",
                "pdflatex",
                "pdflatex"
            ]
        },
    ],
    "latex-workshop.latex.clean.fileTypes": [
        "*.aux",
        "*.bbl",
        "*.blg",
        "*.idx",
        "*.ind",
        "*.lof",
        "*.lot",
        "*.out",
        "*.toc",
        "*.acn",
        "*.acr",
        "*.alg",
        "*.glg",
        "*.glo",
        "*.gls",
        "*.ist",
        "*.fls",
        "*.log",
        "*.fdb_latexmk"
    ],
    "latex-workshop.latex.autoClean.run": "onFailed",
    "latex-workshop.latex.recipe.default": "lastUsed",
    "latex-workshop.view.pdf.internal.synctex.keybinding": "double-click"
}
```

```
{
	// Place your snippets for latex here. Each snippet is defined under a snippet name and has a prefix, body and 
	// description. The prefix is what is used to trigger the snippet and the body will be expanded and inserted. Possible variables are:
	// $1, $2 for tab stops, $0 for the final cursor position, and ${1:label}, ${2:another} for placeholders. Placeholders with the 
	// same ids are connected.
	// Example:
	// "Print to console": {
	// 	"prefix": "log",
	// 	"body": [
	// 		"console.log('$1');",
	// 		"$2"
	// 	],
	// 	"description": "Log output to console"
	// }
	 "fraction": {
		"prefix": "fr",
		"body": [
			"\\frac{$1}{$2} ",
		 ],
		 "description": "fraction"
	}, 
	 "partial fraction": {
		"prefix": "pf",
		"body": [
			"\\frac{\\partial $1}{\\partial $2} $3",
		 ],
		 "description": "partial fraction"
	}, 
	"partial fraction 2": {
		"prefix": "pft",
		"body": [
			"\\frac{\\partial^2 $1}{\\partial {$2}^2} $3",
		 ],
		 "description": "partial fraction"
	}, 
	 "left right ()": {
		"prefix": "le",
		"body": [
			"\\left( $1\\right) $2",
		 ],
		 "description": "big()"
	}, 
	 "power": {
		"prefix": "dj",
		"body": [
			"^{$1} ",
		 ],
		 "description": "^{}"
	}, 
	 "underline": {
		"prefix": "ud",
		"body": [
			"_{$1} $2",
		 ],
		 "description": "_{}"
	}, 
	"and": {
		"prefix": "and",
		"body": [
			"& $1",
		 ],
		 "description": "&"
	},
	"cdot": {
		"prefix": "cd",
		"body": [
			"\\cdot $1",
		 ],
		 "description": "cdot"
	},
	"cdots": {
		"prefix": "cs",
		"body": [
			"\\cdots $1",
		 ],
		 "description": "cdots"
	},
	 "listing": {
		"prefix": "ls",
		"body": [
			"$1_1,$2_2,\\ldots,$3_n $4",
		 ],
		 "description": "x_1,x_2,...,x_n"
	}, 
	 "fig": {
		"prefix": "fig",
		"body": [
			"\\begin{figure}[!ht]\n    \\centering\n    \\includegraphics[$2]{$1}\n    \\caption{$3}\n    \\label{$4}\n\\end{figure}",
		],
		"description": "fig"
	}, 
	"infty": {
		"prefix": "inf",
		"body": [
			"\\infty $1",
		],
		"description": "infty"
	}, 
	"int upper inf": {
		"prefix": "ininf",
		"body": [
			"\\int^\\infty_{$1} $2",
		],
		"description": "infty"
	}, 
	"suminf": {
		"prefix": "suminf",
		"body": [
			"\\sum^\\infty_{$1} $2",
		],
		"description": "sum upper infty"
	}, 
	"table": {
		"prefix": "tab",
		"body": [
			"\\begin{table*}[!ht]\n    \\caption{$1}\n    \\vspace*{3pt}\n    \\renewcommand\\arraystretch{1.5}\n    \\centering\n    \\begin{tabular}{p{3cm}<{\\centering}p{3cm}<{\\centering}p{1.5cm}<{\\centering}p{1.5cm}<{\\centering}}\n        \\toprule\n        $2&&& \\\\\\ \n        \\midrule\n        $3&&& \\\\\\\n        \\bottomrule\n    \\end{tabular}\n\\end{table*}\n$4",
		],
		"description": "table"
	}, 
	"overline": {
		"prefix": "ov",
		"body": [
			"\\overline{$1}$2",
		],
		"description": "overline"
	}, 
	"vec": {
		"prefix": "vec",
		"body": [
			"\\overrightarrow{$1}$2",
		],
		"description": "overrightarrow"
	}, 
	"alpha": {
		"prefix": "alp",
		"body": [
			"\\alpha ",
		],
		"description": "alpha"
	}, 
	"beta": {
		"prefix": "bet",
		"body": [
			"\\beta ",
		],
		"description": "beta"
	}, 
	"phi": {
		"prefix": "phi",
		"body": [
			"\\varphi ",
		],
		"description": "phi"
	}, 
	"pi": {
		"prefix": "pi",
		"body": [
			"\\pi ",
		],
		"description": "pi"
	}, 
	"mu": {
		"prefix": "mu",
		"body": [
			"\\mu ",
		],
		"description": "mu"
	}, 
	"int": {
		"prefix": "int",
		"body": [
			"\\int",
		],
		"description": "int"
	}, 
	"zeta": {
		"prefix": "zet",
		"body": [
			"\\zeta ",
		],
		"description": "zeta"
	}, 
	"lim_0": {
		"prefix": "lim0",
		"body": [
			"\\lim_{$1 \\rightarrow 0} $2",
		],
		"description": "lim x -> 0"
	}, 
	"lim_inf": {
		"prefix": "linf",
		"body": [
			"\\lim_{$1 \\rightarrow \\infty} $2",
		],
		"description": "lim x -> oo"
	}, 
	"liomega": {
		"prefix": "om",
		"body": [
			"\\omega ",
		],
		"description": "omega"
	}, 
	"frame": {
		"prefix": "frame",
		"body": [
			"\\begin{frame}[fragile]{$1}\n    $2\n\\end{frame}\n",
		],
		"description": "frame environment"
	}, 
	"cols": {
		"prefix": "cols",
		"body": [
			"\\begin{columns}\n$1\n\\end{columns}",
		],
		"description": "columns environment"
	}, 
	"col": {
		"prefix": "col",
		"body": [
			"\\begin{column}{$1\\textwidth}\n$2\n\\end{column}$3",
		],
		"description": "column environment"
	}, 
	"height": {
		"prefix": "hei",
		"body": [
			"height = $1 \\textheight - $2 cm",
		],
		"description": "height"
	}, 
	"width": {
		"prefix": "wid",
		"body": [
			"width = $1 \\textwidth - $2 cm",
		],
		"description": "wid"
	}, 
	"item": {
		"prefix": "it",
		"body": [
			"\\begin{itemize}\n    \\item $1 \n\\end{itemize}",
		],
		"description": "itemize"
	}, 
	"CJK": {
		"prefix": "cjk",
		"body": [
			"\\begin{CJK*}{UTF8}{gbsn}\n    $1 \n\\end{CJK*}",
		],
		"description": "CJK-song"
	}, 
	"Noindentqquad": {
		"prefix": "nq",
		"body": [
			"\\noindent\\qquad ",
		],
		"description": "缩进"
	}, 
	"define": {
		"prefix": "ejgs",
		"body": [
			"\\begin{ejgs}\\textbf{$1}\\\\\\\n    \\phantom{占位} $2 \n\\end{ejgs}",
		],
		"description": "ejgs环境"
	}, 
	"Delta": {
		"prefix": "del",
		"body": [
			"\\Delta",
		],
		"description": "Delta"
	}, 
	"delta": {
		"prefix": "delta",
		"body": [
			"\\delta",
		],
		"description": "delta"
	},
	"rho": {
		"prefix": "rho",
		"body": [
			"\\rho ",
		],
		"description": "rho"
	},
	"BoldinMath": {
		"prefix": "cu",
		"body": [
			"\\textit{\\textbf{$1}} ",
		],
		"description": "bold"
	},
	"Boldinalpha": {
		"prefix": "calp",
		"body": [
			"\\boldsymbol{$1} ",
		],
		"description": "bold"
	},
	"dd frac": {
		"prefix": "df",
		"body": [
			"\\frac{\\mathrm{d} $1}{\\mathrm{d} $2} ",
		],
		"description": "dd frac"
	},
	"times": {
		"prefix": "ch",
		"body": [
			"\\times ",
		],
		"description": "times"
	},
	"varepsilon": {
		"prefix": "ep",
		"body": [
			"\\varepsilon ",
		],
		"description": "varepsilon"
	},
	"varepsilon_0": {
		"prefix": "ep0",
		"body": [
			"\\varepsilon_0 ",
		],
		"description": "varepsilon_0"
	},
	"varepsilon_r": {
		"prefix": "epr",
		"body": [
			"\\varepsilon_r ",
		],
		"description": "varepsilon_r"
	},
	"dwk": {
		"prefix": "dwk",
		"body": [
			"\\frac{1}{4 \\pi \\varepsilon _{0} } ",
		],
		"description": "大学物理的k"
	},
	"sigma": {
		"prefix": "sig",
		"body": [
			"\\sigma ",
		],
		"description": "sigma"
	},
	"partial": {
		"prefix": "par",
		"body": [
			"\\partial ",
		],
		"description": "partial"
	},
	"sintefblue": {
		"prefix": "sint",
		"body": [
			"\\bf\\large\\color{sintefblue}",
		],
		"description": "sintefblue"
	},
	"bfsintefblue": {
		"prefix": "bs",
		"body": [
			"\\bf\\color{sintefblue}",
		],
		"description": "bfsintefblue"
	},	
	"align*": {
		"prefix": "ali",
		"body": [
			"\\begin{align*}\n    $1\n\\end{align*}\n",
		],
		"description": "align*"
	},
	"sqrt": {
		"prefix": "sq",
		"body": [
			"\\sqrt{$1}",
		],
		"description": "sqrt"
	},
	"lnot": {
		"prefix": "ln",
		"body": [
			"\\lnot ",
		],
		"description": "lnot"
	},
	"wedge": {
		"prefix": "wl",
		"body": [
			"\\wedge ",
		],
		"description": "wedge"
	},
	"vee": {
		"prefix": "lw",
		"body": [
			"\\vee ",
		],
		"description": "vee"
	},
	"overbar": {
		"prefix": "ba",
		"body": [
			"\\overline{$1} ",
		],
		"description": "overline"
	}
}

```


### 参考资料

- [Visual Studio Code (vscode)配置LaTeX - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/166523064)

- [Latex+VSCode 正向搜索和反向搜索 | Jintao Lee (jintaolee-roger.github.io)](https://jintaolee-roger.github.io/posts/latexsearch/)
