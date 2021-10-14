## Name
Simplenoteクローン

## Author
* 小野寺剣人
* ジーズアカデミーDev21
* twitter: https://twitter.com/kntonodera
* facebook: https://www.facebook.com/profile.php?id=100057938040349

## Usage 
0. 前提条件<br>
* node.jsのインストール
* MAMPのインストール
1. kentoOnodera/php04ファイルをダウンロード(このフォルダ)<br>
2. 任意のフォルダを作成
3. Laravel6系のインストール<br>
2で作成した[任意のフォルダ]配下で下記コマンドを入力<br>
composer create-project laravel/laravel simplenote "6.0.*" --prefer-dist<br>

4. .envをの下記のように記入<br>
DB_CONNECTION=mysql<br>
DB_HOST=[自身のMAMPを確認]<br>
DB_PORT=[自身のMAMPを確認]<br>
DB_DATABASE=simplenote<br>
DB_USERNAME=[自身のMAMPを確認]<br>
DB_PASSWORD=[自身のMAMPを確認]<br>
DB_SOCKET=/Applications/MAMP/tmp/mysql/mysql.sock<br>
※MAMPにて実装しているためDB_HOST、DB_PORT、DB_USERNAME、DB_PASSWORDは自身のローカル環境を確認<br>

5. Laravel/UIのインストール<br>
2で作成した[任意のフォルダ]配下で下記コマンドを入力<br>
composer require laravel/ui "^1.2"<br>

6. 1でダウンロードしたフォルダを[任意のフォルダ]にドラック＆ドロップ<br>
置き換えますか？と聞かれたら置き換える

7. MAMPをスタート<br>

8. サーバー立ち上げ<br>
[任意のフォルダ]配下で下記コマンドを入力<br>
php artisan serve<br>

9. 自信のMAMP環境にアクセス<br>
例)http://127.0.0.1:8000/<br>

10.ログインで下記を入力<br>
【E-Mail Address】 kento.onodera@dakara.work<br>
【Password 】kento626<br>

## File
1. コントローラーにて基本処理を実装<br>
app/HTTP/Controllers/HomeController.php

2. 基本処理の共通化<br>
app/HTTP/AppServiceProvider

3. メインのレイアウトテンプレート<br>
resources/views/layouts/app.blade.php

4. ログイン、新規登録のレイアウトテンプレート<br>
resources/views/layouts/auth.blade.php

5.  ホームのブレード<br>
resources/views/home.blade.php

6. noteの追加用ブレード<br>
resources/views/create.blade.php

7. すでにあるnoteの編集用ブレード<br>
resources/views/edit.blade.php

8. DB情報<br>
* TagのDB
  app/Tag.php<br>
  app/databese/maigration/2021_10_12_044152_create_memos_table.php


* MemoのDB
  app/Memo.php<br>
  2021_10_12_044334_create_tags_table.php

* MemoとTagのリレーショナルのためにmemosにtag_idを追加<br>
app/databese/maigration/2021_10_14_054122_add_tag_id_to_memos_table

 
## Reference
https://www.youtube.com/watch?v=NLqO2b3xEW0&t=5228s

## My growth
* Laravel基礎理解
* MVCモデル
* リレーショナルデータベースがすごい!





