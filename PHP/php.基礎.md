php基礎
-開始タグ　終了タグ
(終了タグは省略できる）
```
<?php

?>
```
・変数の指定
$をつけて宣言
```
$msg = "Hello World";
echo $msg;
#=> Hello World
```
・var_dumpで型を確認できる
```
$msg = "Hello World";
var_dump($msg);
#=> string(11) "Hello World"
```
・文字列
"ダブルクォーテーション"か'シングルクォーテーション'で宣言できる
-"ダブルクォーテーション"の場合
変数展開できる
```
$name = "ren";

echo "My name is $name";
echo "My name is ${name}";
echo "My name is {$name}";
#=> My name is ren
```
-'シングルクォーテーション'の場合
.(ドット）を使うことで文字列を結合できる
```
echo 'My name is '.$name;
#=> My name is ren
```
・配列
作成
```
$colors = array("red","blue","yellow");
$colors = ["red","blue","yellow"];
```
取得
```
echo $colors[0];
#=> red
```
