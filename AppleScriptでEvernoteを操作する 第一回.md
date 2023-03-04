---
title : AppleScriptでEvernoteを操作する 第一回
link : 22564
date : Sat, 22 Jul 2017 02:14:53 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","〈学びの土曜日〉"]
draft : false
author : 倉下忠憲
---

さて、今回からEvernoteをAppleScriptで操作するための講座をお送りします。基礎的な知識をご紹介しますので、Evernoteの活用にお役立てください。

<h2>AppleScript</h2>

まず肝心要のAppleScriptですが、乱暴にまとめれば、Macのアプリケーションを操作するための簡易スクリプト言語、といったところ。
※詳細は、<a href="https://ja.wikipedia.org/wiki/AppleScript">AppleScript</a>(Wikipedia)を参照のこと

Macなら標準でインストールされていますので、誰でも無料で使えます。で、わりかし簡単です。

このAppleScripを使って、Evernoteをわちゃわちゃしてやろう、というのが一つの目標です。

<h2>なぜ使うの？</h2>

具体的な操作に入る前に、まず、なぜAppleScriptを利用するのかですが、AppleScriptを使うと、以下の二つができるようになります。

<ul>
<li>処理の自動化</li>
<li>データを他のアプリケーションに受け渡し</li>
</ul>

前者はたとえば、同じようなノートを365枚作成する場合、手動では当然365回Evernoteを操作しなければいけないわけですが、AppleScriptを使えばそれが一瞬でできます。また、後者については、用途が実に多様ですが、一例を挙げておけば、テキストエディタに書いた内容を使ってEvernoteにノートを作成したり、Evernoteのノート情報を利用して、OmniOutlinerに項目を作ったり、といったことができます。これも便利です。

最終的な使い方はその人次第になりますし、自分次第の使い方ができるからこそAppleScrptでの操作を覚える意義があるわけですが、本連載は、ごくごく基本的な記述方法について語ることで、その導入になることを目指します。

では、次回から具体的な記述方法について入っていきましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/515rWUhPqbL._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.07.22</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 236,150<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.07.22</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 1,284<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
