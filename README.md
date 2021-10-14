## Name
Simplenoteクローン

## Features
Laravelにてsimplenoteっぽいのを実装

## Usage 

基本処理の共通化
app/HTTP/AppServiceProvider

###基本処理
app/HTTP/Controllers/HomeController.php

###メインのレイアウトテンプレート
resources/views/layouts/app.blade.php

###ログイン、新規登録のレイアウトテンプレート
resources/views/layouts/auth.blade.php

###noteの追加用ブレード
resources/views/create.blade.php

###noteの追加用ブレード
resources/views/create.blade.php

###すでにあるnoteの編集用ブレード
resources/views/edit.blade.php

###ログインした直後にアクセスするブレード
resources/views/edit.blade.php

###DB情報
####TagのDB
app/Tag.php
app/databese/maigration/2021_10_12_044152_create_memos_table.php


####MemoのDB
app/Memo.php
2021_10_12_044334_create_tags_table.php

####MemoとTagのリレーショナルのためにmemosにtag_idを追加
app/databese/maigration/2021_10_14_054122_add_tag_id_to_memos_table

## Author
* 小野寺剣人
* ジーズアカデミーDev21
 
## Reference
https://www.youtube.com/watch?v=NLqO2b3xEW0&t=5228s

### 今回の課題で特に勉強になったこと
* Laravel基礎理解
* MVCモデル
* リレーショナルデータベースがすごい!





