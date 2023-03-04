---
title : WorkFlowyを、たためるテキストエディタに
link : 18897
date : Wed, 07 Sep 2016 00:31:03 +0000
categories : ["アウトライナーで遊ぼう","writingmethod"]
tags : ["workflowy","アウトライナー・ライティング","アウトライナー概論"]
draft : false
author : 倉下忠憲
---

小さいところから始めるとき、大がかりな道具よりも普段使い慣れたこぢんまりした道具を手にした方がスムーズに進めやすいことがあります。

文章の構造を考えるときも、まず手書きでラフに書くようにテキストエディタに要素を書き並べていく。構造化の印（しるし）として、マークダウンの書式を置いておく。これだけでも、階層が二つぐらいならば容易に把握できます。

<a href="https://rashita.net/blog/?attachment_id=18898" rel="attachment wp-att-18898"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot1-500x394.png" alt="screenshot" width="500" height="394" class="alignnone size-medium wp-image-18898" /></a>

あとは上から下までを見ながらちょくちょく書き足していけばいいだけです。

しかしながら、ここに大量に書き込み始めると途端に視認性・操作性が悪くなります。「下の階層の文章は表示のオン・オフを切り替えたい」。そんな願いも湧いてきます。

そうですね。アウトライナーの出番というわけです。

<h3>通常の表記では……</h3>

しかしながら、WorkFlowyにそれをポンと投げ込み、表示をたためるようにそれを下位の構想に配置してしまうと、当然のように段落が下がります。これはもう、見事に下がります。視認性においてはもちろん有用なのですが、テキストエディタ的なフラットさはなくなってしまいました。

<a href="https://rashita.net/blog/?attachment_id=18901" rel="attachment wp-att-18901"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot3-500x358.png" alt="screenshot" width="500" height="358" class="alignnone size-medium wp-image-18901" /></a>

それがいいんだよ、という声もあるでしょうが、私としてはテキストエディタを使っている感覚の延長線上で、テキストをたたみたいのです。

そうですね。Stylishの出番です。

※Stylishについては以下の記事を参照。
<a href="https://rashita.net/blog/?p=15453">R-style » 『Stylish』でWorkflowyの見た目をカスタマイズした</a>
<a href="https://rashita.net/blog/?p=16896">R-style » WorkFlowyのスタイルを「matFlow.dark」に変更</a>
<a href="https://rashita.net/blog/?p=15464">R-style » Workflowyでnoteを全文表示にしてみた</a>
<a href="http://cyblog.jp/modules/weblogs/18812">WorkFlowyでハイライトを使えるようにカスタマイズする方法 | シゴタノ！</a>

<h3>flatOutliner</h3>

ベースは、「WorfFlowy for Writers」。左寄せにして、バレットを消してくれるスタイルです。さらにこのスタイルの子の左マージンをマイナスに指定します。

<a href="https://rashita.net/blog/?attachment_id=18902" rel="attachment wp-att-18902"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot4-500x191.png" alt="screenshot" width="500" height="191" class="alignnone size-medium wp-image-18902" /></a>

Append 

<code>.selected>.children>.project .project{margin-left: -27px ;margin-bottom:3px;}</code>

そうしてできあがったのが、これ。

<a href="https://rashita.net/blog/?attachment_id=18903" rel="attachment wp-att-18903"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot5-500x213.png" alt="screenshot" width="500" height="213" class="alignnone size-medium wp-image-18903" /></a>

一見すると普通のテキストエディタですが、機能的にはちゃんと構造を有しています。だから、（下位には見えませんが）下位の項目を閉じたり、開いたりできます。

<a href="https://rashita.net/blog/?attachment_id=18904" rel="attachment wp-att-18904"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot6-500x192.png" alt="screenshot" width="500" height="192" class="alignnone size-medium wp-image-18904" /></a>
※たとえば1を閉じた

簡易ではありますが、「たためるテキストエディタ」の完成です。

<h3>さいごに</h3>

もちろん、この表示は、アウトラインを操作したい場合には非常に使いにくいのでご注意下さい。

何事も適材適所です。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51HoJpXhvnL._SL160_.jpg" alt="アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.09.07</div></div><div class="amazlet-detail">技術評論社 (2016-07-09)<br />売り上げランキング: 26,878<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00XCIETIG/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41WikKyn%2BuL._SL160_.jpg" alt="アウトライン・プロセッシング入門: アウトライナーで文章を書き、考える技術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00XCIETIG/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">アウトライン・プロセッシング入門: アウトライナーで文章を書き、考える技術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.09.07</div></div><div class="amazlet-detail"> (2015-05-07)<br />売り上げランキング: 745<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00XCIETIG/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51ymv5zS94L._SL160_.jpg" alt="クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.09.07</div></div><div class="amazlet-detail">インプレスR&D (2016-01-29)<br />売り上げランキング: 1,476<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

