# ショートカット

* Ctrl + Shift + P でコマンドパレットを開く
* keyboard shortcuts fileと入力し、keybindings.json を開く
* 以下を入力し再起動

```
// Place your key bindings in this file to overwrite the defaults
[
{ "key": "ctrl+a",  "command": "editor.action.selectAll",
                       "when": "editorTextFocus && !inDebugRepl" },
{ "key": "ctrl+c",   "command": "editor.action.clipboardCopyAction",
                       "when": "editorTextFocus && !inDebugRepl && vim.mode != 'Insert'" },
{ "key": "ctrl+n",  "command": "workbench.action.files.newUntitledFile",
                       "when": "editorTextFocus && !inDebugRepl && vim.mode != 'Insert'" },
{ "key": "ctrl+v",  "command": "editor.action.clipboardPasteAction",
                       "when": "editorTextFocus && !inDebugRepl && vim.mode == 'Insert'" },
{ "key": "ctrl+w",  "command": "workbench.action.closeActiveEditor",
                       "when": "editorTextFocus && !inDebugRepl && vim.mode != 'Insert'" },
{ "key": "ctrl+x",  "command": "editor.action.clipboardCutAction",
                       "when": "editorTextFocus && !inDebugRepl" }
]
```

補足
* ctrl+a: テキストの全選択
* ctrl+c: 選択したテキストをクリップボードにコピー(Insert Mode ではないとき)。
* ctrl+n: 新規ファイルを開く(Insert Mode ではないとき)。
* ctrl+v: クリップボードの内容をペースト(Insert Mode のみ)
* ctrl+x: 選択したテキストをクリップボードに切り取り
* ctrl+w: ファイル(タブ)を閉じる(Insert Mode のみ)

