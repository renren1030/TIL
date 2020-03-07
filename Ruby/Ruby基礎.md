# Rubyとは　

-オブジェクト指向言語
全てにメソッドが使えるということ  


-メソッド呼び出し
オブジェクト.メソッド（引数１,引数２,引数３）  
オブジェクト.メソッド 引数１,引数２,引数３  
オブジェクト.メソッド

-文字列の連結は足し算<br>
式展開を使ってもいい#{式} ※ただし""で囲う　''では適用されない
```
name = "Alice" 
puts "Hello,#{name}!" #=>Hello,Alice!
```
```
name = "Alice" 
puts 'Hello,#{name}!' #=>Hello,#{name}! そのまま出力される
```
```
name = "Alice" 
puts 'Hello'+ name'!'#=>Hello,Alice! 式展開使わずに。見にくい。
```
-絶対値にはabsメソッドを使う
```
1.abs #=> 1
-10.abs #=> 10

a = 10
b = -50

(a * b).abs #=> 500

1.1.abs #=> 1.1
-4.3.abs #=> 4.3
```
-upcaseメソッド（小文字を大文字に）
```
puts "hello world".upcase #=>	"HELLO WORLD"
```
-downcaseメソッド（大文字から小文字に）
```
puts "WHAT IS THIS".downcase #=>"what is this"
```
-swapcaseメソッド（小文字を大文字、大文字を小文字に）
```
puts "ibc BootCamp".swapcase #=>	"IBC bOOTcAMP"
```
-capitalizeメソッド（先頭の小文字を大文字に）
```
puts "ruby on rails".capitalize` #=>"Ruby on rails"
``
