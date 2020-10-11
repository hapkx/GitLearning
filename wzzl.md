### 美赛资料整理

+ 美赛题目汇总：[历年试题](https://www.shumo.com/wiki/doku.php?id=%E7%BE%8E%E5%9B%BD%E5%A4%A7%E5%AD%A6%E7%94%9F%E6%95%B0%E5%AD%A6%E5%BB%BA%E6%A8%A1%E7%AB%9E%E8%B5%9B_mcm_icm_%E5%8E%86%E5%B9%B4%E8%AF%95%E9%A2%98)

+ 美赛O奖论文汇总：[MCM-ICM](https://www.shumo.com/wiki/doku.php?id=%E7%BE%8E%E5%9B%BD%E5%A4%A7%E5%AD%A6%E7%94%9F%E6%95%B0%E5%AD%A6%E5%BB%BA%E6%A8%A1%E7%AB%9E%E8%B5%9B_mcm_icm_%E5%8E%86%E5%B9%B4%E8%AF%95%E9%A2%98)

+ VSCode写LaTex环境配置：[Visual Studio Code (vscode)配置LaTeX](https://zhuanlan.zhihu.com/p/166523064)
  + 配置文件：[配置详解](https://github.com/James-Yu/LaTeX-Workshop/wiki/Compile)

```json
	// latex configuration
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
        {
            "name": "XeLaTeX",  // 对不同字体支持的比较好，但编译的时候比较慢
            "tools": [
                "xelatex"
            ]
        },
        {
            "name": "PDFLaTeX", // 只会用默认字体替换pdf中的字体，但编译速度很快
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
    "team.showFarewellMessage": false,
    "workbench.sideBar.location": "left",
    "latex-workshop.message.update.show": false,

    // default pdf viewer: tab/external/broswer. 
    "latex-workshop.view.pdf.viewer": "tab",
    "latex-workshop.view.pdf.ref.viewer": "auto",

    // configure progress bar 
    "latex-workshop.progress.enabled": true,
    "latex-workshop.progress.location": "Status Bar",
    "latex-workshop.progress.runIconType": "Solid Circled",
    "latex-workshop.progress.barStyle": "Block Quadrants",
    "latex-workshop.progress.barLength": 48,
```



