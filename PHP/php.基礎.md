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
・変数に数字を足す
```
足す値が１の時だけ、省略して書くことができる
$x += 1 →　＄x++;
$x -= 1 →　＄x--;
```
```
++を変数の前に書くとその行の命令が実行される前に足されるのに対して、++を変数の後に書くとその行の命令が実行された後に足される（--でも同様）
$x = 3;
$y = 3;
echo ++$x;
#=> 4
echo $y++;
#=> 3(echoの後に+1される）
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
・そのほか
```
$name = "Nakamura";
$name .= "Ren";
echo $name;
#=> NakamuraRen
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
追加
```
$colors = array("red","blue","yellow");
$colors[] = "green";
echo $colors[3]
#=> green
```
・連想配列
```
$user = array("name" => "Ren","age" => 20);
echo $user["name"]
#=> Ren
```
追加
```
$user["level"]="beginner
・条件分岐
if文
```
$x = 20;
if($x > 30){
 echo"$xは3０より大きい"；
}elseif($x >= 20){
 echo"$xは２０以上３０以下"
}else{
 echo"$xは２０より小さい"；
}
#=> $xは２０以上３０以下
```
switch文
caseのブロックの最後にbreakを実行しないと後ろに続くcase文が実行されてしまう。
```
switch($coin){
 case 0:
  echo"表";
  break;
 case 1:
  echo"裏";
  break;
 default:
  echo"エラー";
  break;
}
```
  
