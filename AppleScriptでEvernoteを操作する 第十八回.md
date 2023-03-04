---
title : AppleScriptでEvernoteを操作する 第十八回
link : 23500
date : Sat, 09 Dec 2017 02:40:46 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23461" title="AppleScriptでEvernoteを操作する 第十七回 – R-style">前回</a>は、Evernoteのノートの中身を取得する方法を紹介しました。

今回は、それを書き換える方法を紹介します。

<h2>狙いとコード</h2>

既存のノートを書き換えるといろいろややこしいので、ノートを新規作成して、そのノートの中身を書き換えてみましょう。コードは以下のようになります。

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with text &quot;this is sample note&quot;
	set anoteText to HTML content of anote
	set anoteText to &quot;hello Evernote&quot; &amp; anoteText
	set HTML content of anote to anoteText
end tell
[/code]

これを実行すると、次のようなノートが作成されるはずです。二行目で、新規ノートを作成し、三行目でその中身を変数に取得して、四行目で、その変数に"hello Evernote"を追記した上で、その変数を作成したノートの中身として設定してあります。

<a href="https://rashita.net/blog/?attachment_id=23501" rel="attachment wp-att-23501"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-9.png" alt="" width="407" height="329" class="alignnone size-full wp-image-23501" /></a>

イメージとしては、ノートの中身を取り出し、それに改変を加えて、ノートの中身として戻す、という感じ。

で、ここで使っているのはHTMLなので、次のようなこともできます。

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with text &quot;this is sample note&quot;
	set anoteText to HTML content of anote
	set anoteText to &quot;&lt;h1&gt;hello Evernote&lt;/h1&gt;&quot; &amp; anoteText
	set HTML content of anote to anoteText
end tell
[/code]

実行すると、次のようなノートが作成されるはずです。

<a href="https://rashita.net/blog/?attachment_id=23502" rel="attachment wp-att-23502"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-10.png" alt="" width="450" height="336" class="alignnone size-full wp-image-23502" /></a>

そうです。Evernoteのエディタでは、文字サイズを大きくすることはできても、h1などの見出しタグの設定はできませんが、こうしてスクリプトを使えば、きちんとした書式を当てることができます。ノートをエクスポートして、別の何かに利用する場合は、書式設定が生きてくるので、なかなか便利です。

h1~6タグだけでなく、bやiやblockquoteなども使えますし、スタイルを直書きすれば、それも（ある程度は）反映されます。

たとえば、以下のように書けば、

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with text &quot;this is sample note&quot;
	set anoteText to HTML content of anote
	set anoteText to &quot;&lt;h1 style=\&quot;color:red;\&quot;&gt;hello Evernote&lt;/h1&gt;&quot; &amp; anoteText
	set HTML content of anote to anoteText
end tell
[/code]

次のようなノートが作成されるでしょう。これを使えば、凝ったデザインのノートも作成可能です。

<a href="https://rashita.net/blog/?attachment_id=23503" rel="attachment wp-att-23503"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-11.png" alt="" width="362" height="335" class="alignnone size-full wp-image-23503" /></a>

一点注意があるとすれば、スタイルを直に書くときは、文中に出てくる " をエスケープしておく必要がある、という点です。以前もたしか説明しましたね。まあ、難しいことは考えずに、" の部分を \" としておけばOKです。

<h2>Next Step</h2>

というわけで、今回はノートの中身をごっそり書き換える方法を紹介しました。もともと用意されているコマンドだと、「新規ノートの作成」（create note）か「一番下に追記」（append）しか実行できないのですが、この方法を使えば、もう少し細かい編集が可能となります。もちろん、多少なりともHTMLやCSSの知識が必要なことは言うまでもありません。

さて、次回は、HTML content of ではなく、ENML content of を使った中身の変更について紹介してみます。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.09</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 144<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.09</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 77,522<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
