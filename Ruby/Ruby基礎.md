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
