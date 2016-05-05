# atom / git / GitHub

## atom 講義 【5分】
### 知っている人を聞く
* atom 使ったことある人ー
* 横のフォルダツリー使ったことある人ー
* 画面の分割できる人ー
* シンタックスハイライトできる人ー

### atom とは
GitHub製のエディタ sublimeみたいなやつ

### フォルダツリーとは
左にある、フォルダの構造が俯瞰できるやつ

### 画面の分割
1つのウィンドウ内を分割して複数のファイルを見ることができる

### シンタックスハイライト
その言語の文法に従って色をつけたりしてくれる


　
## git 講義 【30分】
### git とは
> プログラムのソースコードなどの変更履歴を記録・追跡するための分散型バージョン管理システムである。
> Linuxカーネルのソースコード管理に用いるためにリーナス・トーバルズによって開発され、それ以降ほかの多くのプロジェクトで採用されている。

### Dropboxとの違い
ファイル更新したら同時に編集してる人のが消えますね。
だめです。
gitならそれぞれの変更点をいい感じにマージしてくれます

### Google Docsとの違い
お互いの影響がすごく出る。
テストもクソもない。
gitならそれぞれの作業を独立した世界で行うことができる

### 実際にgitで管理されているコードに触れてみよう
`$ git clone https://github.com/sesta/proken_sample.git`

### 何かを変更してその変更を保存しよう
1. さっきcloneしたディレクトリをatomで開く
2. `git-test-ユーザ名.md`を新しく作って1行で自己紹介
3. `$ git status` - 現在の変更を確認
4. `$ git add ファイル名` - 変更を保存したいファイルを指定
5. `$ git status` - 現在の変更を確認
6. `$ git commit -m バージョンの説明` - 変更をバージョンとして保存
7. `$ git log` - 今までのバージョンの確認
8. できてる！

### いろいろやったが、これが若干わかりやすい
http://qiita.com/yunico-jp/items/87bdd13971e82833f6bb


　
## GitHub 講義 【20分】
### GitHubとは
> ソフトウェア開発プロジェクトのための共有ウェブサービスであり、Gitバージョン管理システムを使用する。

### githubに鍵を登録しよう
1. github にログイン
2. 設定の`SSH and GPG keys`ってのを見てみる、何もないよね？
3. `$ key-gen`
4. エンター3連打
5. `$ pbcopy < ~/.ssh/id_rsa.pub`
6. 設定ページに戻って`New SSH Keys`
7. `$ ssh github.com` Hi！ とか言われるはず

### 変更をプッシュしてみよう
1. `$ git pull origin master`
2. `$ git push origin master`
3. 怒られたら1からもっかい
4. `https://github.com/sesta/proken_sample` にアクセス！


　
## 参考になりそうなURLたち
### エディタ比較
* http://radcules.com/【超おすすめ】エディター比較「sublimetext」と「atom」と/
### 郵便局メソッド
* http://qiita.com/yunico-jp/items/87bdd13971e82833f6bb
### githubの鍵登録
* http://monsat.hatenablog.com/entry/generating-ssh-keys-for-github
