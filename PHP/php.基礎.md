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
（caseのブロックの最後にbreakを実行しないと後ろに続くcase文が実行されてしまう。）

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
break文
（ループを強制終了させる）
```
for($i=1;$<=10;$++){
 if($i > 5){
  break;
  }
  echo $i;
 }
 #=> 12345
 ```
 continue文
 （break文と違いループしているところだけ抜ける）
 ```
 for($i=1;$<=10;$++){
 if($i % 3 ==0){
  continue;
  }
  echo $i;
 }
 #=> 1234567810(３の倍数以外）
 ```
 foreach文
 （配列や連想配列に対してデータを取り出すために用いる）
 
 ```
 foreach(配列(連想配列）as (キー変数 =>)値変数）{
 　繰り返したい処理;
  }
 ```
 ・関数
 strlen(文字列の文字数を返す関数）
 ```
 $language = "PHP";
 echo strlen($language);
 #=> 3
```
count(配列の要素数を返す関数）
```
$number = array(1,2,3);
echo count($number);
#=> 3
```
他にも色々ある

・関数の作り方
```
function 関数名(){処理}
()の中には引数を指定できる
```
関数の呼び出し方
```
関数名（）
```
```
function sum($num1,$num2){
echo $num1 + $num2;
}
sum(1,3);
#=> 4
```
戻り値
```
function sum($num){
return $num*$num*3;
}
$Pi = sum(3);
echo $Pi;
#=> 27
```
・フォームデータを受け取る
```
echo $_POST["キー名"];
$_POSTは連想配列になっている
```
