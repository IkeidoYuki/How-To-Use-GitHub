# GitHubを使う前にこのファイルを読むこと

## 0.事前準備
### Gitのインストール
以下URLより、Gitのインストールを行う  
https://gitforwindows.org/

インストール完了後、PowerShellを起動して以下コマンドを実行する。  
`git --version`

想定結果  
`git version 2.31.0.windows.1`

### Gitの初期設定
PowerShellを起動し、以下コマンドを実行する  
```
git config --global user.name ★任意のユーザー名★
git config --global user.email ★メールアドレス★
```

### GitHubのアカウント作成
以下URLにアクセスし、アカウントを作成する  
https://github.com/  

## Gitの操作  
### ① 最初に実施する内容  
Gitの初期化 (ローカルリポジトリの作成)  
```
git init
```

リモートリポジトリのファイルをローカルリポジトリにコピー  
```
git clone <リモートリポジトリのURL>
```

### ② ローカルのファイルをアップロードする場合  
通常はマスターブランチ (大元)から、自身でブランチを切る。
```
git branch -b master/ブランチ名
```

ローカルのファイル編集後、以下コマンドでGitHubにMergeする。  
最初に編集したローカルファイルを以下コマンドでaddする。  
```
git add <編集したファイル名>
```
ここで、全てのローカルファイルをaddする場合、以下コマンドとなる。
```
git add -A
```

次にファイルをcommitする。  
```
git commit -m "ファイル編集者につたえたい文言"

git commit -m "[add] ファイル名や日付が一般的"
```

ここで変更履歴については、以下コマンドを実行することで確認ができる。  
gitのステータス確認
```
git status
```

gitの差分確認
```
git diff
```

gitの変更履歴確認
```
git log
```

ローカルで作成したファイルをリモートにpushし、Merge Requestを作成する。
```
git remote add origin GitHubのURL
git push origin master
```




## 参考文献
https://tech-blog.rakus.co.jp/entry/20200529/git  
https://web-camp.io/magazine/archives/75359  
https://backlog.com/ja/git-tutorial/stepup/11/  
