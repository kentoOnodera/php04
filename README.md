## Name
Simplenoteクローン

## Features
Laravelにてsimplenoteっぽいのを実装

## Usage 
1. Laravel6系のインストール<br>
composer create-project laravel/laravel simplenote "6.0.*" --prefer-dist

2. .envをの下記のように記入<br>
　※MAMPにて実装しているためDB_HOST、DB_PORT、DB_USERNAME、DB_PASSWORDは自身のローカル環境を確認<br>
DB_CONNECTION=mysql
DB_HOST=[自身のローカル環境を確認]
DB_PORT=[自身のローカル環境を確認]
DB_DATABASE=simplenote
DB_USERNAME=[自身のローカル環境を確認]
DB_PASSWORD=[自身のローカル環境を確認]
DB_SOCKET=/Applications/MAMP/tmp/mysql/mysql.sock

3. Laravel/UIのインストール
composer require laravel/ui "^1.2"


## file
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

## Author
* 小野寺剣人
* ジーズアカデミーDev21
 
## Reference
https://www.youtube.com/watch?v=NLqO2b3xEW0&t=5228s

## 今回の課題で特に勉強になったこと
* Laravel基礎理解
* MVCモデル
* リレーショナルデータベースがすごい!





