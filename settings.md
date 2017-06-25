# 初期セッティング手順

## golangインストール
* http://golang-jp.org/doc/install
* 自分の環境用のインストール手順を参照
* 本レポジトリのGo言語は、 `go version go1.8.3`

## githubの設定(Mac / Win)
* http://github.com にユーザ登録

### Macの場合

#### .gitconfigファイルの設定
* ターミナルを開く
* `$ cd ~`
* `$ vim .gitconfig`
* 以下を記述
```
[user]
        name = {Github.comのユーザ名}
        email = {登録したメールアドレス}
[push]
        default = simple
[core]
        precomposeunicode = true
        quotepath = false
```
* 保存して終了 (:wq)

#### SSHキーの設定
* `$ cd ~/.ssh`
* `$ ls -al`
  * [id_rsa]ファイルがすでに作られていた場合は次の操作が変わる
* `$ ssh-keygen`
  * [id_rsa]ファイルがなかった場合
    * 色々質問されるが全てエンターでOK
  * あった場合
    * 最初の質問でファイル名を入力(後はエンター)
* https://github.com/settings/keys にアクセス
* `New SSH key`ボタンをクリック
* [Title]にPCの名前とか入れておくと後で楽
* [Key]には以下のコマンドの出力結果をコピペする
  * `$ cat id_rsa.pub` 

### Windowsの場合
[参照](http://www.granfairs.com/blog/staff/gitbash-setting-shortcut)

## git clone
* `$ cd ~`
* `$ mkdir repos`
* `$ cd repos`
* `$ git clone git@github.com:SotaroYamane/study-golang.git`
