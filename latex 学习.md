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



### 参考资料

- [Visual Studio Code (vscode)配置LaTeX - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/166523064)

- [Latex+VSCode 正向搜索和反向搜索 | Jintao Lee (jintaolee-roger.github.io)](https://jintaolee-roger.github.io/posts/latexsearch/)