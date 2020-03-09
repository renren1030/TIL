配列　まとめ<br>
.配列の作成
```
array = [] 
# []
array = [1,2,3] 
# [1,2,3]
```
・要素を連続させたい時
```
範囲オブジェクト.to_a
```
```
 (1..5).to_a
# [1,2,3,4,5]
```
要素の取得
```
array  = ["a","b","c",nil]

p array[0]
#"a"

p array[1..2]
#["b","c"]
```
要素の追加　
<<を使うことで末尾に追加できる
pushメソッドも同様
```
array  = ["a","b","c","d"]
array[4] = "e"

p array
#["a", "b", "c", "d", "e"]

array.push("f")
p array
#["a", "b", "c", "d", "e", "f"]

array << 'hoge'
p array
#["a", "b", "c", "d", "e", "f", "hoge"]
```
・要素の更新
```
array  = ["a","b","c","d"]
array[0] = "e"

p array
#["e", "b", "c", "d"]
```
・要素の削除
```
array  = ["a","b","c","d","f"]
array.delete("a");

p array
#["b", "c", "d","f"]

#[index番号, 削除する個数]で指定
array[0,3] = []
p array
#["f"]
```
・配列の要素を結合し文字列として作成
```
array  = ['ruby','javascript','php','python']
newArray = array.join(',')
p newArray
#"ruby,javascript,php,python"
```
・各要素に対してブロック評価をした後、新しい配列を返す
```
a1 = [100, 200, 300]
a2 = a1.map { |x| x * 2 }
p a2 # [200, 400, 600]
```
・要素の選択、絞り込み
```
array = (1..12).to_a
p array.select {|a| a % 2==0}

#[2, 4, 6, 8, 10, 12]
```
・要素の重複の削除
```
array = [1,1,2,2,2,3,4,4,5,8]
p array.uniq

#[1, 2, 3, 4, 5, 8]
```
・様々なメソッド
-push（末尾に追加）,pop(末尾を削除）
```
array  = ["a","b","c","d","e"]
array.push(1);
p array
#["a", "b", "c", "d", "e", 1]

array.pop
p array
#["a", "b", "c", "d", "e"]
```
-unshift(先頭に追加）,shift(先頭を削除）
```
array  = ["a","b","c","d","e"]
array.unshift(1);
p array
#[1, "a", "b", "c", "d", "e"]

array.shift
p array
#["a", "b", "c", "d", "e"]
```
