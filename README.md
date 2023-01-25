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



## 参考文献
https://tech-blog.rakus.co.jp/entry/20200529/git  
https://web-camp.io/magazine/archives/75359  
https://backlog.com/ja/git-tutorial/stepup/11/  
