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
    "latex-workshop.view.pdf.internal.synctex.keybinding": "double-click",
    "editor.fontSize": 20,
    "editor.wordWrap": "on",
    "latex-workshop.view.pdf.viewer": "legacy",
    "security.workspace.trust.untrustedFiles": "open",
    "gitlens.views.drafts.avatars": false,
    "[latex]": {
        "editor.defaultFormatter": "lenagain.latexindent"
    },
    "http.noProxy": [
        ""
    ],
    "http.proxy": "socks://127.0.0.1:7897",
    "http.proxySupport": "on",
    "git.autofetch": true,
    "git.openRepositoryInParentFolders": "always",
    "todo-tree.tree.showScanModeButton": false,
    "todo-tree.filtering.excludeGlobs": [
        "**/node_modules",
        "*.xml",
        "*.XML"
    ],
    "todo-tree.filtering.ignoreGitSubmodules": true,
    "todohighlight.keywords": [],
    "todo-tree.tree.showCountsInTree": true,
    "todohighlight.keywordsPattern": "TODO:|FIXME:|NOTE:|\\(([^)]+)\\)",
    "todohighlight.defaultStyle": {},
    "todohighlight.isEnable": false,
    "todo-tree.highlights.customHighlight": {
        "BUG": {
            "icon": "bug",
            "foreground": "#F56C6C",
            "type": "text"
        },
        "FIXME": {
            "icon": "flame",
            "foreground": "#FF9800",
            "type": "tag-and-comment"
        },
        "TODO": {
            "foreground": "#FFEB38",
            "type": "line"
        },
        "NOTE": {
            "icon": "note",
            "foreground": "#67C23A",
            "type": "whole-line"
        },
        "INFO": {
            "icon": "info",
            "foreground": "#909399",
            "type": "text-and-comment"
        },
        "TAG": {
            "icon": "tag",
            "foreground": "#409EFF",
            "type": "line"
        },
        "HACK": {
            "icon": "versions",
            "foreground": "#E040FB",
            "type": "line"
        },
        "XXX": {
            "icon": "unverified",
            "foreground": "#E91E63",
            "type": "line"
        }
    },
    "todo-tree.general.tags": [
        "BUG",
        "HACK",
        "FIXME",
        "TODO",
        "INFO",
        "NOTE",
        "TAG",
        "XXX"
    ],
    "todo-tree.general.statusBar": "total"
}