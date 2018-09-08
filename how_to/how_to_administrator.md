# 管理者用情報
ここには管理者向け情報をまとめます。

## 翻訳者の追加方法

**注意: 最初に個人のアカウントを作っておかないと、transifexに招待できないようです。**

- Slackで依頼を貰ったら、[transifex](https://www.transifex.com/)にログインします。
- ヘッダーの「チーム」を選択します。
- 「協力者を招待」ボタンをクリックします。

![admin_invite_01](../images/readme/admin_invite_01.png)

- 協力者のアカウント、協力者の役割「レビューアー」、チーム名の選択「pyladies-handbook-translation team」、言語を選択「Japanese(ja)」を選択
- 「招待を送る」をクリックします。

![admin_invite_02](../images/readme/admin_invite_02.png)

翻訳者がアカウントを登録すると、チーム概要画面に「承認待ちの参加申請」リンクが出るのでクリックします。

![admin_invite_03](../images/readme/admin_invite_03.png)

承認します。

![admin_invite_04](../images/readme/admin_invite_04.png)

## transifexの利用方法
[transifex](https://www.transifex.com/) を利用し、翻訳を行うための手順を記述します。

### 本家のpyladies-kitから翻訳用ファイルを作成

手元に [pyladies-kit](https://github.com/pyladies/pyladies-kit) を `clone` する。

仮想環境を作り、Sphinxをインストールします。

```bash
$ pip install Sphinx
$ pip install sphinx-intl
```

`docs/` に移動

conf.pyを書き換え（ファイルの最後に追加）

```python
locale_dirs = ["locale"]
language = "ja"
```

potファイルを作成するコマンドを実行

```bash
$ make gettext
```

`_build/locale` の下に `*.pot` ファイルができている

potファイルからpoファイルを作る

```bash
$ sphinx-intl update -p _build/locale -l de -l ja
```

ここまでで、拡張子が `po` のファイルが作成されますので、これをtansifexのリソースに追加します。

transifexを利用して、翻訳してください。

### 翻訳後のファイルを日本語版ドキュメントファイルに戻す

`locale/ja/LC_MESSAGES/` に翻訳したpoファイルを戻す

htmlファイルを作成する

```bash
$ make -e html
```

完成！

ここまでの流れは、以下にあります。
- [国際化 — Sphinx 1.5.6 ドキュメント](http://www.sphinx-doc.org/ja/stable/intl.html)
- [(3日目) Sphinx の文書を翻訳してみよう (gettext機能) - Hack like a rolling stone](https://tk0miya.hatenablog.com/entry/20111203/p1) に殆ど書いてあります。
- [翻訳作業って何をするの? — Elliptium](http://tink.elliptium.net/2017/02/27/actual_translation_work.html)
