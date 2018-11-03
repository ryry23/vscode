# php-cs-fix

## 前提

* Windows
* phpをインストール済み

## 手順

### php-cs-fixer.bat

- composerをインストール
  - https://getcomposer.org/doc/00-intro.md#installation-windows (ページ下部)
- 任意のフォルダに下記内容のファイルを設置し、installコマンドを実行
- composer.json配下にvendor/bin/php-cs-fixer.batが作成されていたら成功

```
# cat composer.json

{
  "require": {
  "friendsofphp/php-cs-fixer": "^2.13"
  }
}

 # composer install
```
### php-cs-fixer.phar

- 下記よりダウンロードした、php-cs-fixer.pharを指定のフォルダへ配置する
  - https://cs.sensiolabs.org/
  - C:\Users\<USER>\.vscode に配置

### php-cs-fixer

- vscode上でctrl + shift + xを入力し、拡張機能を呼び出す
  - php-cs-fixerをインストールする
- ctrl + shift + pからユーザ設定を開く
  - 画面上部にsettings.jsonと入力すれば、settings.jsonを編集と出てくるのでそれを選択
  - 以下設定を入力し完了

  ```
    //php-cs-fixer settings
  "php-cs-fixer.executablePath": "${extensionPath}\\php-cs-fixer.phar",
  "php-cs-fixer.executablePathWindows": "<composer.jsonのパス>\\vendor\\bin\\php-cs-fixer.bat",   //eg: php-cs-fixer.bat
  "php-cs-fixer.onsave": false,
  "php-cs-fixer.rules": "@PSR2",
  "php-cs-fixer.config": ".php_cs;.php_cs.dist",
  "php-cs-fixer.allowRisky": false,
  "php-cs-fixer.pathMode": "override",
  "php-cs-fixer.exclude": [],
  "php-cs-fixer.autoFixByBracket": true,
  "php-cs-fixer.autoFixBySemicolon": false,
  "php-cs-fixer.formatHtml": false,
  "php-cs-fixer.documentFormattingProvider": true,
  "php-cs-fixer.lastDownload": 1541262881396
  ```