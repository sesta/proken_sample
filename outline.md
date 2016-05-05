# atom / git / GitHub

## atom 講義 【5分】
1. 知っている人を聞く
  * atom 使ったことある人ー
  * 横のフォルダツリー使ったことある人ー
  * 画面の分割できる人ー
  * シンタックスハイライトできる人ー

2. atom とは
3. フォルダツリーとは
4. 画面の分割
5. シンタックスハイライト


## git 講義 【20分】
1. git とは
> プログラムのソースコードなどの変更履歴を記録・追跡するための分散型バージョン管理システムである。
> Linuxカーネルのソースコード管理に用いるためにリーナス・トーバルズによって開発され、それ以降ほかの多くのプロジェクトで採用されている。

2. Dropboxとの違い
  ファイル更新したら同時に編集してる人のが消えますね
    だめです

3. Google Docsとの違い
  お互いの影響がすごく出る
    テストもクソもない

4. 実際にgitで管理されているコードに触れてみよう
`$ git clone https://github.com/sesta/proken_sample.git`

5. 何かを変更してその変更を保存しよう
  1. さっきcloneしたディレクトリをatomで開く
  2. `git-test-ユーザ名.md`を新しく作って1行で自己紹介
  3. `$ git status`
  4. `$ git add ファイル名`
  5. `$ git status`
  6. `$ git commit -m バージョンの説明`
  7. `$ git log`
  8. できてる！

6. いろいろやったが、これが若干わかりやすい
http://qiita.com/yunico-jp/items/87bdd13971e82833f6bb


## GitHub 講義 【10分】
1. GitHubとは
> ソフトウェア開発プロジェクトのための共有ウェブサービスであり、Gitバージョン管理システムを使用する。

2. githubに鍵を登録しよう
  1. github にログイン
  2. 設定の`SSH and GPG keys`ってのを見てみる、何もないよね？
  3. `$ key-gen`
  4. エンター3連打
  5. `$ pbcopy < ~/.ssh/id_rsa.pub`
  6. 設定ページに戻って`New SSH Keys`
  7. `$ ssh github.com`
    Hi！ とか言われるはず

3. 変更をプッシュしてみよう
  1. `$ git pull origin master`
  2. `$ git push origin master`
  3. 怒られたら1からもっかい
  4. `https://github.com/sesta/proken_sample` にアクセス！
