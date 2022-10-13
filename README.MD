# WordPress local

Macの状態をメモ

```shell
sw_vers

ProductName:    macOS
ProductVersion: 12.6
BuildVersion:   21G115
```

MAMP v6.3(1040)

## MAMPにWordPressをインストールする

### WordPressのダウンロード

[WordPress を入手](https://ja.wordpress.org/download/)

WordPress 6.0.2

### MAMPにWordPressをインストールする

/Applications/MAMP/htdocs の直下に `wp-local`フォルダを作成する

ダウンロードしたWordPressを解凍して、中身を全て`wp-local`へ移動する（wordpressフォルダは不要）

### MAMPを起動してDBを作成する

MAMPがデフォルト設定なら下記から作成できる。
localhostを指定している場合は適宜読み替えるようにしてください。

http://localhost:8888/phpMyAdmin/index.php?lang=ja

ここではデータベース名は`wp_local`に設定します。

DBのデフォルトは

user: root
pass: root

### WordPressをインストールする

上記設定通りなら下記にアクセスすると初期画面が表示されます。
クリックして進めてください。

http://localhost:8888/wp-local/


- データベース名: wp_local
- ユーザー名: root
- パスワード: root
- データベースのホスト名: localhost
- テーブル接頭辞: wp_

で作成します。

サイトのタイトル: wp-local
ユーザー名: root
パスワード: root
メールアドレス: 会社のアドレス

以上で終了。

## テーマの接続を確認する

`mytheme`フォルダ内に

- index.php
- style.css
- screenshot.png : 880 x 660 のpng画像

を作成します。

index.php

```php
<!DOCTYPE html>
<html lang="ja">
<head>
  <meta charset="UTF-8">
  <meta http-equiv="X-UA-Compatible" content="IE=edge">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Document</title>
</head>
<body>
  テスト
</body>
</html>
```

style.css

```css
/*
Theme Name: wp-local
Theme URI:
Description: 
Author: 
Author URI: 
Version: 0.0
Tags:
License: CC BY 2.1 JP
License URI: https://creativecommons.org/licenses/by/2.1/jp/
Last Update 2022-10-13
*/
```