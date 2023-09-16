# Visual Studio Code Setting

```json
{
  // 同步更新至：https://gist.github.com/oneleo/780d90384b6444e504b8a7b2fc49f9e5
  // -----------------------------
  // ----------- VSCode -----------
  // -----------------------------
  // 滑鼠點選其他分頁時，舊分頁自動存檔
  "files.autoSave": "onFocusChange",
  // 調整字體大小
  "editor.fontSize": 15,
  // 文字超過螢幕自動挪到下一行
  "editor.wordWrap": "on",
  // 存檔前先按照「./.prettierrc」格式工具設定檔格式再存檔
  "editor.formatOnSave": true,
  // 使用 Prettier 做為 VSCode 預設的格式化工具
  "editor.defaultFormatter": "esbenp.prettier-vscode",
  // 設置輸入特定字元時是否自動顯示提示
  "editor.suggestOnTriggerCharacters": true,
  // 設置按下 tab 鍵時輸出 space 還是 tab 鍵（註：存檔後仍會被 Lint 設置複寫）
  "editor.insertSpaces": false,
  // 承上，若選擇輸出 space，則設置要輸出幾個 space
  "editor.tabSize": 4,
  // 承上，是否要根據編輯的檔案自動偵測要輸入的 space 數量
  "editor.detectIndentation": false,
  // 設置在哪邊輸入特殊字元時自動顯示提示
  "editor.quickSuggestions": {
    "strings": "on",
    "comments": "on",
    "other": "on"
  },
  // 為 ESLint 提供者啟用自動修復
  "editor.codeActionsOnSave": {
    "source.fixAll.eslint": true
  },
  // 控制是否要為搜尋結果顯示行號。
  "search.showLineNumbers": true,
  // 若模式為全小寫，搜尋時不會區分大小寫; 否則會區分大小寫
  "search.smartCase": true,
  // 設置搜尋結果顯示上限，null = 無上限
  "search.maxResults": null,
  // 設置搜尋欄的位置
  "search.actionsPosition": "auto",
  // 設置搜尋欄的顯示方式
  "search.defaultViewMode": "tree",
  // 啟用時，新的搜尋編輯器會重複使用先前所開啟之搜尋編輯器的包含、排除與旗標
  "search.searchEditor.reusePriorSearchConfiguration": true,
  // 建立新的搜尋編輯器時，要使用的周圍內容預設行數
  "search.searchEditor.defaultNumberOfContextLines": 2,
  // 控制搜尋檢視應讀取或修改 macOS 上的共用尋找剪貼簿
  "search.globalFindClipboard": true,
  // 控制新的 [搜尋: 在檔案中尋找] 及 [在資料夾中尋找] 作業發生位置: 在搜尋檢視或在搜尋編輯器中
  "search.mode": "newEditor",
  // 允許在使用中的編輯器沒有選取項目時，從最接近游標的文字植入搜尋
  "search.seedWithNearestWord": true,
  // 是否在 Quick Open 的檔案結果中，包含全域符號搜尋中的結果
  "search.quickOpen.includeSymbols": true,
  // 是否顯示上方的 tabs
  "workbench.editor.showTabs": true,
  // 設置上方 tabs 寬度的最大值及最小值
  "workbench.editor.tabSizing": "fixed",
  "workbench.editor.tabSizingFixedMaxWidth": 180,
  "workbench.editor.tabSizingFixedMinWidth": 180,
  // 設置上方 pined tabs 的寬度
  "workbench.editor.pinnedTabSizing": "normal",
  // 設置上方 tabs 的關閉鈕位置
  "workbench.editor.tabCloseButton": "right",
  // 未存檔的 tabs 高亮顯示
  "workbench.editor.highlightModifiedTabs": true,
  // 設置最上方 tabs 顯示 1 列或多列
  "workbench.editor.wrapTabs": true,
  // 修改顯示新 tabs 的順序
  "workbench.editor.openPositioning": "right",
  // vscode 使用黑暗主題
  "workbench.colorTheme": "Default Dark+",
  // 點選左側檔案時，一律開新分頁
  "workbench.editor.enablePreview": false,
  // 設置多選按鍵
  "workbench.list.multiSelectModifier": "ctrlCmd",
  "workbench.colorCustomizations": {
    // 修改程式碼左側對齊線的顏色
    "editorIndentGuide.background1": "#404040"
  },
  // 預設使用 pnpm 包管理器
  "npm.packageManager": "pnpm",
  // -----------------------------
  // -------- TailwindCSS --------
  // -----------------------------
  "files.associations": {
    "*.css": "tailwindcss"
  },
  // -----------------------------
  // --------- TypeScript ---------
  // -----------------------------
  "[typescript, javascript, json]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "vscode.typescript-language-features"
  },
  // -----------------------------
  // ----------- React -----------
  // -----------------------------
  "[typescriptreact, javascriptreact]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  // -----------------------------
  // ----------- Svelte -----------
  // -----------------------------
  "[svelte]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "svelte.svelte-vscode"
  },
  "svelte.enable-ts-plugin": true,
  // -----------------------------
  // ------------ CSS ------------
  // -----------------------------
  "[css, scss]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  // -----------------------------
  // ---------- Solidity ----------
  // -----------------------------
  "solidity.telemetry": false,
  // 指定 *.sol 使用的格式化工具
  "[solidity]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "NomicFoundation.hardhat-solidity"
    // "editor.defaultFormatter": "JuanBlanco.solidity"
  },
  // -----------------------------
  // ----------- Python -----------
  // -----------------------------
  // Python 語言
  "[python]": {
    "editor.formatOnType": true
  },
  // -----------------------------
  // --------- Haskell ---------
  // -----------------------------
  "[haskell]": {
    "editor.formatOnSave": true,
    "editor.defaultFormatter": "esbenp.prettier-vscode"
  },
  // -----------------------------
  // --------- Codeium AI ---------
  // -----------------------------
  "codeium.enableSearch": true,
  "diffEditor.hideUnchangedRegions.enabled": true
  // -----------------------------
  // -- The End of the Settings --
  // -----------------------------
}
```
