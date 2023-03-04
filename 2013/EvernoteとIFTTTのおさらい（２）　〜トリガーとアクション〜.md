---
title : EvernoteとIFTTTのおさらい（２）　〜トリガーとアクション〜
link : 12228
date : Mon, 16 Dec 2013 03:21:40 +0000
categories : ["evernoteの使い方"]
tags : ["evernoteとiftttのおさらい","evernote","ifttt"]
draft : false
author : 倉下忠憲
---

今回は、IFTTTのメインイベントでもある「トリガー」と「アクション」の紹介に入ってみましょう。

※前回まで
第一回：<a href="https://rashita.net/blog/?p=12150" target="_blank">EvernoteとIFTTTのおさらい（１）　〜IFTTTとは何か〜</a>

まずは、Evernoteのチャンネルが持つトリガーとアクションを取り上げます。
<H3>Evernoteトリガー</H3>「もしAしたらBする」

のAにあたるのがトリガーでしたね。

残念ながら、Evernoteが持つトリガーはたった一種類しかありません。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot24.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot24.png" alt="screenshot" width="350" height="297" class="alignnone size-full wp-image-12229" /></a>

「New shared note link」（新しくノートリンクがシェアされたら）

Evernoteに「ノートリンク」という機能がありますが、それのことではありません。簡単に言えば、ノートがシェアされたときです。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot25.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot25.png" alt="screenshot" width="500" height="428" class="alignnone size-full wp-image-12230" /></a>

上のボタンからSNSに投稿したり、ノートをメールでシェアしたりできますが、そういう場合に作成されるのがpublic note link。これが生まれたときに何かする、というのがEvernoteが唯一持つトリガーです。

つまり、

「もしAしたらBする」

のAに埋められるのが「ノートをシェア」だけなのです。

正直、あまり活用度は高くありません。そもそも、ノートのシェア自体、現時点ではあまり使われていないでしょう。

それでも何かしら用途はあるかもしれないので、一応頭の片隅に置いておいてください。

<H3>Evernoteアクション</H3>「もしAしたらBする」

のBにあたるのがアクションです。

IFTTTとEvernoteの連携を考える上で、メインとなるのはこちらでしょう。なぜかというと、何かの「アーカイブ」として機能するのがEvernoteです。他のサービスでの活動をEvernoteでログとして保存する。こういう使い方はごくナチュラルな運用になりそうです。

そのEvernoteが持つアクションは次の５つ。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot26.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot26.png" alt="screenshot" width="500" height="260" class="alignnone size-full wp-image-12231" /></a>

「Create note」（ノートを新規作成する）
「Append to note」（ノートに追記する）
「Create a link note」（URLソースを含んだノートを新規作成する）
「Create image note from URL」（URLにある画像を含んだノートを新規作成する）
「Create an audio note from URL」（URLにある音声ファイルを含んだノートを新規作成する）

大きく分けて、二つのアクションがあることに気がつかれたでしょう。

一つが「ノートを新規作成する」。こちらは、URLや画像を含んだバリエーションがいくつかあります。

※URLソースを含んだノートの例
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot27.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot27.png" alt="screenshot" width="500" height="90" class="alignnone size-full wp-image-12233" /></a>

もう一つは「ノートに追記する」。こちらはバリエーションがありません。単にノートに追記するだけ。

とりあえずEvernoteアクションの全体像をつかんでください。「ノートを新規作成する」か「既存のノートに追記するか」。この二つです。どちらも大いに有効です。

たとえば、「自分がお気に入りを付けたツイートをEvernoteのノートに保存する」というレシピならば、前者が使えます。対して、「iOSのリマインダーで処理済みにしたものをEvernoteのノートで一覧できるようにする」というレシピなら後者です。

新しくノートを作るのか。既存のノートに追記していくのか。

それぞれの具体的な中身については次回に譲りますが、どういうレシピを作ればいいのかをイメージする際には、この二つの違いについて注意してください。

<H3>ちなみに、Twitterチャンネルでは？</H3>比較として、Twitterチャンネルが持つトリガーとアクションも簡単に紹介しておきましょう。

トリガー
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot28.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot28.png" alt="screenshot" width="500" height="260" class="alignnone size-full wp-image-12236" /></a>

「New tweet by you」（あなたがツイートしたら）
「New tweet by you with hashtag」（あなたがハッシュタグツイートをしたら）
「New tweet by you in area」（あなたが位置情報付きツイートをしたら）
「New link by you」（あなたがリンク付きツイートをしたら）
「New favorite tweet by you」（あなたがツイートをお気に入りにしたら）

アクション
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot29.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot29.png" alt="screenshot" width="500" height="260" class="alignnone size-full wp-image-12237" /></a>

「Post a Tweet」（ツイートを投稿する）
「Post a Tweet with image」（画像付きツイートを投稿する）
「Add user to list」（リストにユーザーを加える）
「Update profile picture」（プロフィール画像を変更する）
「Update bio」（プロフィール情報を変更する）

これで、Evernoteと合わせて６のトリガーと10のアクションが揃いました。これだけでも、さまざまなレシピを作成することができます。

新しくノートリンクがシェアされたら→ツイートを投稿する
新しくノートリンクがシェアされたら→プロフィール情報を変更する
あなたがツイートしたら→ノートを新規作成する
・・・
・・
・

<H3>さいごに</H3>基本的にどのチャンネルでも同じ考え方でレシピを作れます。

まずは各チャンネルがどのようなトリガーとアクションを持っているのかを確認してみてください。

次回は、アクションの具体的な中身について解説していきます。

次回→<a href="https://rashita.net/blog/?p=12242" target="_blank">EvernoteとIFTTTのおさらい（３）　〜アクションの中身〜</a>
