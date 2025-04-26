# 1es_report_assignment
1esレポート

以下Vscode設定
```json
{
  // ---------- Language ----------
  "[bibtex]": {
    "editor.suggest.snippetsPreventQuickSuggestions": false,
    // インデント幅を2にする
    "editor.tabSize": 2
  },
  "markdown-preview-enhanced.hideDefaultVSCodeMarkdownPreviewButtons": false,
  // LaTeX
  "latex-workshop.intellisense.package.enabled": true,
  //補助配流を自動的に削除
  "latex-workshop.latex.autoClean.run": "onBuilt",
  //削除する補助ファイルを追加
  //latexmkのビルドレシピ
  "latex-workshop.latex.recipes": [
    //bibTexを使用しない場合のレシピ
    {
      "name": "ptex2pdf (uplatex)*2",
      "tools": ["ptex2pdf (uplatex)", "ptex2pdf (uplatex)"]
    },
    //bibTexを使用する場合のレシピ
    {
      "name": "ptex2pdf (uplatex) -> bibtex -> ptex2pdf (uplatex) *2",
      "tools": [
        "ptex2pdf (uplatex)",
        "pbibtex",
        "ptex2pdf (uplatex)",
        "ptex2pdf (uplatex)"
      ]
    }
  ],
  //latexmkのビルドツール
  "latex-workshop.latex.tools": [
    {
      "name": "ptex2pdf (uplatex)",
      "command": "ptex2pdf",
      "args": [
        "-interaction=nonstopmode",
        "-l",
        "-u",
        "-ot",
        "-kanji=utf8 -synctex=1",
        "%DOC%"
      ]
    },
    {
      "name": "pbibtex",
      "command": "pbibtex",
      "args": ["%DOCFILE%"]
    }
  ],
  //これより下の設定は人それぞれかも
  "latex-workshop.view.pdf.viewer": "tab",
  "latex-workshop.chktex.enabled": false,
  "latex-workshop.latex.autoBuild.run": "onSave",
  "git.autofetch": true,
  "git.enableSmartCommit": true,
  "git.confirmSync": false,
  "AVR.programmer.definitions": "C:/dev/bin/avrdude.conf",
  "AVR.programmer.rate": 9600,
  "AVR.programmer.tool": "C:/dev/bin/avrdude.exe",
  "AVR.programmer.type": "stk500v2",
  "AVR.source.compiler": "C:/dev/bin/avr-c++.exe",
  "AVR.programmer.port": "com8",
  "workbench.colorTheme": "Solarized Light",
  "window.zoomLevel": -1,
  "idf.espIdfPathWin": "C:/Users/106no/esp-idf/",
  "idf.pythonBinPathWin": "C:/Users/106no/.espressif/python_env/idf4.2_py3.8_env/Scripts/python.exe",
  "idf.toolsPathWin": "C:\\Users\\106no\\.espressif",
  "idf.customExtraPaths": "C:\\Users\\106no\\.espressif\\tools\\xtensa-esp32-elf\\esp-2020r3-8.4.0\\xtensa-esp32-elf\\bin;C:\\Users\\106no\\.espressif\\tools\\xtensa-esp32s2-elf\\esp-2020r3-8.4.0\\xtensa-esp32s2-elf\\bin;C:\\Users\\106no\\.espressif\\tools\\esp32ulp-elf\\2.28.51-esp-20191205\\esp32ulp-elf-binutils\\bin;C:\\Users\\106no\\.espressif\\tools\\esp32s2ulp-elf\\2.28.51-esp-20191205\\esp32s2ulp-elf-binutils\\bin;C:\\Users\\106no\\.espressif\\tools\\cmake\\3.16.4\\bin;C:\\Users\\106no\\.espressif\\tools\\openocd-esp32\\v0.11.0-esp32-20220706\\openocd-esp32\\bin;C:\\Users\\106no\\.espressif\\tools\\ninja\\1.10.0;C:\\Users\\106no\\.espressif\\tools\\idf-exe\\1.0.1;C:\\Users\\106no\\.espressif\\tools\\ccache\\3.7;C:\\Users\\106no\\.espressif\\tools\\dfu-util\\0.9\\dfu-util-0.9-win64",
  "idf.customExtraVars": {
    "OPENOCD_SCRIPTS": "C:\\Users\\106no\\.espressif\\tools\\openocd-esp32\\v0.11.0-esp32-20220706/openocd-esp32/share/openocd/scripts",
    "IDF_CCACHE_ENABLE": "1"
  },
  "idf.gitPathWin": "C:/Users/106no/.espressif/tools/idf-git/2.30.1/cmd/git.exe",
  "[cpp]": {
    "editor.defaultFormatter": "ms-vscode.cpptools"
  },
  "editor.formatOnSave": true,
  "editor.mouseWheelZoom": true,

  "markdown-pdf.headerTemplate": "",
  "markdown-pdf.footerTemplate": "",
  "markdown-pdf.printBackground": true,
  "idf.hasWalkthroughBeenShown": true
}

```
