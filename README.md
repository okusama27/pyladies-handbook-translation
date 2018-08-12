# pyladies-handbook-translation

PyLadiesには、[PyLadies Organizer Handbook](http://kit.pyladies.com/) というハンドブックがあります。
このハンドブックの翻訳プロジェクトです。

## 目的
- [PyLadies Organizer Handbook](http://kit.pyladies.com/)の日本語化
- 本家と同様に `pip` コマンドでインストールできるようにする
- 本家ハンドブックに `/ja` として取り込んでもらう

## 方法
翻訳には、`docs.python.org` でも利用されている [transifex](https://www.transifex.com/) を利用します。

## 翻訳者になるには
以下の手順で翻訳に参加します。

- [transifex](https://www.transifex.com/) にアカウントを作成する
- [PyLadies Japan Slack](https://pyladies-japan.slack.com/) の `#handbook-translation` 部屋で [transifex](https://www.transifex.com/) のアカウントを書き込んでください。

**翻訳** と **レビュー** ができるユーザーとして招待します。

不明なことは `#handbook-translation` 部屋で確認してください。

## 翻訳する

「ダッシュボード」を選択し、「翻訳」ボタンをクリックします。

![user_01](images/readme/user_01.png)

言語「Japanese(ja)」を選択します。

![user_02](images/readme/user_02.png)

「未翻訳」が存在する行を選びます。

![user_03](images/readme/user_03.png)

翻訳する行を選びます。右側に翻訳文を入力します。気になることがあったら、「コメント」を書いてください。

![user_04](images/readme/user_04.png)

## レビューする
慣れてきたら、他の人の翻訳をレビューしましょう。

ダッシュボードから、翻訳一覧に移動し、「レビュー待ちの文字列」が存在する行を選びます。

![review_01](images/readme/review_01.png)

左上の「レビュー待ち」の数字をクリックすると、レビュー待ちの一覧が表示されます。
内容を確認し、直に修正するか、コメントを付けましょう。
レビューが終了したら、コメントに **LGTM（Looks Good To Me）** と書いてください。コードレビューなどで使われる自分的にはOKという意味です。
レビューボタンは押さないでください。

![review_02](images/readme/review_02.png)


## 【管理者向け】翻訳者の追加方法

**注意: 最初に個人のアカウントを作っておかないと、transifexに招待できないようです。**

- Slackで依頼を貰ったら、[transifex](https://www.transifex.com/)にログインします。
- ヘッダーの「チーム」を選択します。
- 「協力者を招待」ボタンをクリックします。

![admin_invite_01](images/readme/admin_invite_01.png)

- 協力者のアカウント、協力者の役割「レビューアー」、チーム名の選択「pyladies-handbook-translation team」、言語を選択「Japanese(ja)」を選択
- 「招待を送る」をクリックします。

![admin_invite_02](images/readme/admin_invite_02.png)

翻訳者がアカウントを登録すると、チーム概要画面に「承認待ちの参加申請」リンクが出るのでクリックします。

![admin_invite_03](images/readme/admin_invite_03.png)

承認します。

![admin_invite_04](images/readme/admin_invite_04.png)

## 決まり

- 1つの訳に2つの **LGTM** がついたら、レビューボタンを押して、完了とします。


## 参考資料

- [翻訳作業って何をするの? — Elliptium](http://tink.elliptium.net/2017/02/27/actual_translation_work.html)
- [(3日目) Sphinx の文書を翻訳してみよう (gettext機能) - Hack like a rolling stone](http://tk0miya.hatenablog.com/entry/20111203/p1)