---
title : EvernoteとIFTTTのおさらい（１）　〜IFTTTとは何か〜
link : 12150
date : Fri, 13 Dec 2013 03:00:48 +0000
categories : ["evernoteの使い方"]
tags : ["evernoteとiftttのおさらい","evernote","ifttt"]
draft : false
author : 倉下忠憲
---

下の記事で紹介されているEvernoteとIFTTTの連携は、なかなか便利です。

<a href="http://lifehacking.jp/2013/12/sending-notes-to-evernote-from-twitter/" target="_blank">Evernoteとツイッターをつなぐ@myen機能が終了へ。利用している方は移行作業を</a>(Lifehacking.jp)

工夫すれば、自分だけの使い方をアレンジすることもできるでしょう。

今回は復習の意味も込めて、IFTTTとEvernoteの連携を簡単にまとめてみます。

<H3>IFTTTってなんぞや？</H3>そもそも、IFTTTって何でしょうか。

簡単に言えば、Webサービスの仲介者です。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/20131213110443.jpg"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/20131213110443.jpg" alt="20131213110443" width="480" height="360" class="alignnone size-full wp-image-12151" /></a>

Aというサービスで何かが発生したら、Bというサービスで何かしらの行動を行う。

この間に立つのがIFTTTです。具体的な行動という意味では、IFTTTは何もしません。AとBのサービスの間に立って、パイプラインをつなげるだけです。

<H3>語句・用語</H3>IFTTTでは、AやBなどのサービスを「<strong>Channel</strong>」（チャンネル or チャネル）と呼びます。

原稿執筆時点で登録されているチャンネルは76あり、EvernoteやTwitterを筆頭に、Googleの各サービスやiOS系、DropboxやWordpressなど、有名どころのサービスが押さえられています（<a href="https://ifttt.com/channels" target="_blank">参照</a>）。ライフハック系の情報をチェックしている人ならば、名前を知らないチャンネルの方が少ないでしょう。

これらのチャンネルには、「<strong>Trigger</strong>」と「<strong>Action</strong>」が準備されています。

<em>サービスAで何かが発生する→サービスBで何かしらの行動を行う</em>

前者の「何かが発生する」にあたるのがTriggerであり、後者の「何かしらの行動を行う」がActionです。

一番最初にあげた記事で紹介されていたTwitterとEvernoteの連携で言えば、

<em>ハッシュタグ付きのツイートを流す→その内容でEvernoteにノート作成</em>

「ハッシュタグ付きのツイートを流す」がTriggerで、「その内容でEvernoteにノート作成」がActionです。

それぞれのチャンネルでは、そのサービスに合わせたTriggerやActionが準備されており、それらを組み合わせることによって、さまざまなバリエーションのセットを生み出すことができます。

またIFTTTでは、

Aしたら→Bする

という一連の流れを<strong>Recipe</strong>（レシピ）と呼び、自分が作成したレシピをWebで公開することもできます。また、人気の高いレシピはIFTTT上でも紹介され、それをそのまま自分のレシピとして取り込むこともできます。

確認しておきましょう。

IFTTT・・・サービスとサービスを仲介するサービス
Channel・・・IFTTTで扱えるサービス
Trigger・・・Channelが持つ「もし〜〜したら」の条件
Action・・・Channelが持つ「〜〜する」の行動
Recip・・・「もしAしたら、Bする」という一連のセット

<H3>作成してみる</H3>では、実際にレシピを作成してみます。

まず、IFTTTにアクセスし、上部メニューの「Create」をクリック。

※IFTTTの画面
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot13.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot13-1024x630.png" alt="screenshot" width="500" height="310" class="alignnone size-large wp-image-12155" /></a>

※上部メニューの拡大図
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot14.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot14.png" alt="screenshot" width="499" height="170" class="alignnone size-full wp-image-12156" /></a>

すると、次のような画面が出てきます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot15.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot15.png" alt="screenshot" width="500" height="180" class="alignnone size-full wp-image-12157" /></a>

ifthisthenthat

とありますが、if this then that のことですね。穴埋めのようにこの文章にパーツをはめ込んでいきます。

大まかな流れは、

<ol>
	<li>「もし〜したら」のチャンネルを選ぶ</li>
	<li>そのチャンネルのTriggerを選ぶ</li>
	<li>Triggerの細かい内容を決定</li>
	<li>「〜する」のチャンネルを選ぶ</li>
	<li>チャンネルのActionを選ぶ</li>
	<li>Actionの細かい内容を決定</li>
	<li>最終的な確認および決定</li>
</ol>

というもの。

細かい部分については次回以降で解説しますので、ざっと画像で流れを確認してください。

※1.「もし〜したら」のチャンネルを選ぶ
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot16.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot16.png" alt="screenshot" width="500" height="311" class="alignnone size-full wp-image-12158" /></a>

※2.そのチャンネルのTriggerを選ぶ
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot17.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot17.png" alt="screenshot" width="500" height="327" class="alignnone size-large wp-image-12159" /></a>

※3.Triggerの細かい内容を決定
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot18.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot18.png" alt="screenshot" width="983" height="485" class="alignnone size-large wp-image-12160" /></a>

※Triggerが決定された
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot19.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot19.png" alt="screenshot" width="500" height="193" class="alignnone size-large wp-image-12161" /></a>

※4.「〜する」のチャンネルを選ぶ
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot20.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot20.png" alt="screenshot" width="500" height="360" class="alignnone size-large wp-image-12162" /></a>

※5.チャンネルのActionを選ぶ
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot21.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot21.png" alt="screenshot" width="500" height="295" class="alignnone size-large wp-image-12163" /></a>

※6.Actionの細かい内容を決定
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot22.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot22.png" alt="screenshot" width="500" height="374" class="alignnone size-large wp-image-12164" /></a>

※7.最終的な確認および決定
<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot23.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot23.png" alt="screenshot" width="500" height="323" class="alignnone size-large wp-image-12165" /></a>

<H3>さいごに</H3>IFTTTは、間に立つだけのツールなので、レシピの作成はとても簡単です。

他の人のレシピを取り込むこともできますが、オリジナルのアレンジをするためには、何かしら自分で作成して、その勘所を掴んでおくとよいでしょう。

次回は、TriggerとActionの細かい話に入ります。

→<a href="https://rashita.net/blog/?p=12228" target="_blank">EvernoteとIFTTTのおさらい（２）　〜トリガーとアクション〜</a>