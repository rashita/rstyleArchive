---
title : 7wrinerのその他の機能
link : 24377
date : Sat, 07 Apr 2018 02:29:07 +0000
categories : ["0-知的生産の技術"]
tags : ["7wriner"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=24366" title="タスクを管理する その2:7wrinerの用途 – R-style">前回</a>までの記事で、いくつかの使い方と、そのために必要な操作の紹介ができました。

今回は、それ以外の機能を紹介しようと思うのですが、基本的に優先課題ではないので作りかけのものが大半な点はご了承ください。

<h2>メニュー</h2>

右上の「7wriner」がメニューボタンになっています。

<a href="https://rashita.net/blog/?attachment_id=24379" rel="attachment wp-att-24379"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-45.png" alt="" width="224" height="337" class="alignnone size-full wp-image-24379" /></a>

<h3>preferences</h3>

設定画面ですが、現在一項目しかありません。

TaskModeをonにすると、実行済みタスクが下に送られないようになります。それだけです。

<a href="https://rashita.net/blog/?attachment_id=24389" rel="attachment wp-att-24389"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-54.png" alt="" width="553" height="362" class="alignnone size-full wp-image-24389" /></a>

<h3>full export</h3>

全体の出力です。個別のラインはプレビューモードで選択できますが、すべてを選択することはできません。それを補佐するための機能です。

text,html,opmlの３つから選べますが、たぶんFirefox以外だとうまく表示されないのではないかと思います。

<a href="https://rashita.net/blog/?attachment_id=24391" rel="attachment wp-att-24391"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-55.png" alt="" width="1154" height="594" class="alignnone size-full wp-image-24391" /></a>

<h3>backup download</h3>

バックアップ用のjsonファイルをダウンロードします。

<a href="https://rashita.net/blog/?attachment_id=24380" rel="attachment wp-att-24380"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-46.png" alt="" width="508" height="378" class="alignnone size-full wp-image-24380" /></a>

ただ、昨日まではiOS版がうまく動いておりませんでした。で、今朝ちょこっとコードを書いたので、多少動くようにはなったかと思います（少なくともiPhoneでは動きました）。が、ファイル名の指定などいろいろ面倒があります。

で、以下の記事。

<a href="http://d.hatena.ne.jp/wineroses/20180405/p1" title="Textwellを使って7wrinerをiCloudにバックアップしよう - W&amp;R : Jazzと読書の日々">Textwellを使って7wrinerをiCloudにバックアップしよう | Jazzと読書の日々</a>

<blockquote>iPhoneだとロゴメニューからの「backup download」が効かない。何も起こらない。</blockquote>

まことに申し訳ありません＆ありがとうございます！

ぶっちゃけTextwellを使っている方はこっちでいいんじゃね、と思わないではありません。なんというか、自分のために作ったツールが、こんな風にかわいがってもらえるというのがインターネットのすばらしいところですね。

というわけで、この辺はもう少し改良したいところです。

<h3>import&replace</h3>

バックアップ用ファイルはバックアップなのですから、復旧できなければ意味がありません。そのための機能です。

※空っぽだったライン
<a href="https://rashita.net/blog/?attachment_id=24382" rel="attachment wp-att-24382"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-48.png" alt="" width="1233" height="594" class="alignnone size-full wp-image-24382" /></a>

※確認
<a href="https://rashita.net/blog/?attachment_id=24384" rel="attachment wp-att-24384"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-50.png" alt="" width="603" height="264" class="alignnone size-full wp-image-24384" /></a>

※通知
<a href="https://rashita.net/blog/?attachment_id=24385" rel="attachment wp-att-24385"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-51.png" alt="" width="620" height="261" class="alignnone size-full wp-image-24385" /></a>

※ここでキャンセルすればimportされない
<a href="https://rashita.net/blog/?attachment_id=24386" rel="attachment wp-att-24386"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-52.png" alt="" width="1420" height="651" class="alignnone size-full wp-image-24386" /></a>

※importボタンを押すとこうなる
<a href="https://rashita.net/blog/?attachment_id=24387" rel="attachment wp-att-24387"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-53.png" alt="" width="1254" height="632" class="alignnone size-full wp-image-24387" /></a>

<h2>clear all data</h2>

デリートボタンの全体版です。最終話のまどかのようにすべてのラインを消し去ります。一応sendしたラインだけは残るようになっています。

が、基本的に7wrinerでは操作の「やり直し」ができないので十分に注意して下さい。一度消してしまったデータは普及できません。くれぐれもバックアップファイルをダウンロードしてからためされるのがよろしいかと存じます。

<h2>さいごに</h2>

というわけで、今回は大きめの機能について紹介してみました。実装がわりと手間なので、作り込みが甘い部分については生暖かい目で見ていただけると助かります。

最後にもう一つ、ほとんどまったくできていない「ウィンドウ」があるのですが、それについてはまた来週にでも。

