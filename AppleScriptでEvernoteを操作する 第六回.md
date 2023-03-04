---
title : AppleScriptでEvernoteを操作する 第六回
link : 22828
date : Sat, 02 Sep 2017 02:48:03 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---



<a href="https://rashita.net/blog/?p=22775">前回</a>は、シンプルな「メモ作成ツール」を作ってみました。今回はそれを改造していきます。

<h2>ノートタイトルの入力</h2>

前回のバージョンでは、ノートの作成は可能でしたが、そのタイトルは無題でした。これを変えたいところです。

では、どのようにすればよいのでしょうか。

真っ先に思いつくのが、ユーザーにノートのタイトルを入力してもらい、それを利用してノートを作成するというもの。これならば、新しいプログラムの知識はほとんど必要ありません。前回作成したものを、二回実行すればよいだけです。

<a href="https://rashita.net/blog/?attachment_id=22830" rel="attachment wp-att-22830"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-5-500x223.png" alt="" width="500" height="223" class="alignnone size-medium wp-image-22830" /></a>

[code]
set myAnswer to display dialog &quot;メモのタイトルを入力してね！&quot; default answer &quot;&quot;
set memoTitle to text returned of myAnswer

set myAnswer to display dialog &quot;メモの内容を入力してね！&quot; default answer &quot;&quot;
set memoTxt to text returned of myAnswer

tell application &quot;Evernote&quot;
	create note title memoTitle with text memoTxt
end tell
[/code]

新しい要素は無いので詳しい解説はしませんが、1〜2行目でノートのタイトルをユーザーから入力してもらい、それを変数に格納し、4〜5行目でノートの内容をユーザーに入力してもらってそれも変数に格納する。あとは、それぞれの変数を利用してノートを作成する、という流れです。

<a href="https://rashita.net/blog/?attachment_id=22831" rel="attachment wp-att-22831"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-6.png" alt="" width="424" height="157" class="alignnone size-full wp-image-22831" /></a>

<a href="https://rashita.net/blog/?attachment_id=22832" rel="attachment wp-att-22832"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-7.png" alt="" width="425" height="163" class="alignnone size-medium wp-image-22832" /></a>

<a href="https://rashita.net/blog/?attachment_id=22833" rel="attachment wp-att-22833"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-8.png" alt="" width="401" height="340" class="alignnone size-medium wp-image-22833" /></a>

<h2>自動設定</h2>

しかし、メモを作成する際に、いちいちタイトルをつけるのは面倒ですね。別の方法はないでしょうか。

そこで思いつくのが、時刻の利用です。タイムスタンプは重複することがまずありませんし、メモのアイデンティファイとしても優秀です。それをノートのタイトルに利用する手はどうでしょうか。

たとえば、こんな感じになります。

<a href="https://rashita.net/blog/?attachment_id=22834" rel="attachment wp-att-22834"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-9-500x206.png" alt="" width="500" height="206" class="alignnone size-medium wp-image-22834" /></a>

[code]
set myAnswer to display dialog &quot;メモの内容を入力してね！&quot; default answer &quot;&quot;
set memoTxt to text returned of myAnswer

set memoTitle to (current date) as text

tell application &quot;Evernote&quot;
	create note title memoTitle with text memoTxt
end tell
[/code]

実行すれば、１つだけダイアログが立ち上がり、メモの内容を入力すると、次のようなノートが作成されます。

<a href="https://rashita.net/blog/?attachment_id=22835" rel="attachment wp-att-22835"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-10.png" alt="" width="370" height="331" class="alignnone size-full wp-image-22835" /></a>

複数回実行していただければ、それぞれのノートタイトルが異なっている（それぞれの現在時刻になっている）のがおわかりいただけるでしょう。

さて、ここで新しく登場したのは、current date という要素です。名前が示すとおり現在時刻が入っている（現在時刻のデータを返してくれる）のですが、そのままだとテキストデータとしては扱えないので、as text を添えて、ノートタイトルとして使えるようにしてあります。

あとはその変数を使って、ノートを作成する。簡単ですね。

このcurrent dateは、いろいろ使い勝手があって、時間だけを取り出したり、曜日だけを取り出したり、日付同士を計算したりできるのですが、ここでは現在時刻だけがあればよいので、深入りは避けておきます。興味がある方は、以下のページを読んで研究してみてください。

<a href="http://blog.goo.ne.jp/vallie/e/faab3427d0a5892ac0ae5d88e765f7d4">AppleScript : 日付や時刻を利用する - GameSprit</a>

<a href="http://tonbi.jp/AppleScript/Tips/Date/Time.html">鳶嶋工房 / AppleScript / Tips / 時・分・秒の扱い</a>

<h2>さいごに</h2>

今回はノートタイトルの設定方法を二つ紹介してみました。ユーザー入力がもっとも簡単ですが、使う側からすると手間でしかありません。そこで、時刻の自動入力のようなものが良いのですが、実はもう一つ有効にノートタイトルを設定する方法があります。

それについては次回紹介してみましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.02</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 92,043<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.02</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 6,566<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

