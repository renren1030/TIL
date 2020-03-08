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
```
ブロックを使う配列のメソッド<br>
-mapメソッド(わざわざ空の配列を作らずに新しい処理を指定することで新しい配列を作ってくれる。)
```
配列の要素の文字列を全て数値にする時
array.map{|n| n.to_i}
または
array.map(&:to_i)
※ただしこの書き方はブロック内で演算子を使っている、またはブロック内でメソッドの引数を渡している、
またはブロック内で複数の文を実行している時には使えない。
```
Range(範囲）
a .. b (bも含める）
a ... b (bは含めない）
```
a = [1,2,3,4,5]
a[1..3] #=>[2,3,4]

a = 'abcdefg'
a[1..3] #=>[bcd]
```
n以上m以下　n以上m未満
```関係演算子を使うバージョン
def judge?(number)
 if 0 <= number && number < 100d
end
 judge(-1) #=>false
 judge(1) #=>true
 judge(99) #=>true
 judge(100) #=>false
 ```
 ```Rangeを使うバージョン(見やすい！）
 def judge?(number)
  (1...100).include?(number)
 end
 judge(-1) #=>false
 judge(1) #=>true
 judge(99) #=>true
 judge(100) #=>false
 ```
-indexメソッド
（引数と一致する要素が最初に見つかった時の添字を返す）
```
a = [10, 20, 30, 10, 20, 30]
a.index(30) #=> 2
```
-joinメソッド（配列を連結して一つの文字列にする）
```
array = ['ruby', 'python']
p array.join #=>"rubypython"
```
```区切り文字も指定できる
array = ['ruby', 'python','java']
p array.join(',') #=>"ruby,python,java"
```
```
string = "a Ruby"
puts string.split().join() #=> "aRuby"
（stringからarrayにするためにsplitメソッドを使った）
```
-charsメソッド（文字列に対して使うことで一文字ずつ分解してくれる）
```
"Ruby".chars #=> ["R","u","b","y"]
```
