#gitコマンドまとめ
```
git init
gitにどのディレクトリを使うのかを宣言する
```
```
git add　ファイル名　or git add .
作業ディレクトリからステージングエリア（インデックス）にあげる
```
```
git commit
コミットする
ステージングエリアからリポジトリ（ローカル、リモート）にあげる
```
```
git commit -m "コミット名"
コミットのメッセージを一行に収める
```
```
git log 
コミット履歴の確認
```
```
git log --oneline
コミット履歴をコンパクトに一行で見れる
```
```
git log -p
どこが変更された場所か場所がわかる
```
```
git log --stat
どのファイルが何箇所変更されたかがわかる
```
```
git status
現在の状況を確認できる
```
```
git diff
どこを編集したのかがわかる
```
```
git diff --cached
ステージングエリアに上がっている場合で、コミットでどこが変更されるのかがわかる
```
```
git rm　ファイル名
gitの管理下にあるファイルを削除する
```
```
git mv　移動元ファイル 移動先ディレクトリ
ファイルを移動させる
```
```
git mv 旧ファイル名 新ファイル名
ファイル名の変更
```
```
git commit --amend
直前のコミットメッセージを変更できる
```
```
git reset --hard HEAD
直前(HEAD)の状態に戻る
```
```
git reset --hard HEAD^
直前のコミットの取り消し
一つ前に戻る
```
```
git reset --hard ORIG_HEAD
一番最初の状態に戻る
```
```
git branch
branchの一覧が見れる
```
```
git branch ブランチ名
ブランチの作成
```
```
git checkout ブランチ名
指定したブランチ（ブランチ名）に移動
```
```
git merge ブランチ名
マージさせたいブランチ先（ブランチ名）をマージ（合体）する
```
```
git branch -d ブランチ名
ブランチの削除
```
```
git tag
タグの一覧をみる
```
```
git tag タグ名
直近のコミットに対してタグをつける(簡単に言うとわかりやすい名前をつけるみたいなこと）
```
```
git show
直前のコミットの内容を見れる
```
```
git show タグ名
タグ名のコミットの内容が見れる
```
```
git tag タグ名　commitのID
直近ではないコミットにタグをつける
```
```
git tag -d タグ名
タグの消去
```
```
git config --global alias.短縮名　本来の名前
gitの命令に短縮名（エイリアス）をつける
ex.
git config --global alias.co checkout
git config --global alias.st status
git config --global alias.br branch
git config --global alias.ci commit
```
```
git config -l
エイリアスの一覧が見れる
```
```
git remote add リポジトリ名（よく使われるのはorigin) 追加する場所
リポジトリの作成
```
```
git remote rm リポジトリ名（よく使われるのはorigin)
リポジトリの削除
```
```
git push プッシュ先のファイル名　プッシュしたいファイル名
ex.
git push origin master
(originにmasterをpushする)
origin :デフォルトのリポジトリ名
master :デフォルトのブランチ名
```
