---
title : AppleScriptでEvernoteを操作する 第十九回
link : 23544
date : Sat, 16 Dec 2017 01:26:20 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23500" title="AppleScriptでEvernoteを操作する 第十八回 – R-style">前回</a>は、ノートの内容を取得し、それを書き換える方法を紹介しました。

今回は同じことを、HTMLではなくENMLで行ってみようかと思ったのですが、よく調べてみるとノートのENML content属性はreading onlyだったので、まっすぐには実行できません。残念です。

それでも、ENMLについて知っておくと結構便利なので簡単に紹介しておきましょう。

<h2>狙いとコード</h2>

まず、ENMLの中身を確認してみます。

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with text &quot;this is sample note&quot;
	set anoteText to ENML content of anote
	display dialog anoteText
end tell
[/code]

このコードを実行すると、以下のようなダイアログが表示されるかと思います。

<a href="https://rashita.net/blog/?attachment_id=23546" rel="attachment wp-att-23546"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-17.png" alt="" width="411" height="164" class="alignnone size-full wp-image-23546" /></a>

これがEvernoteのノートの中身です。

基本的にはHTMLと同じですが、この<en-note>の中では、いくつかの特殊なタグが使えます。その中で、一番利用価値が高いのが<en-todo/>です。

たとえば、以下のようなコードを実行してみましょう。

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with enml &quot;&lt;en-todo/&gt;this is Task&quot;
end tell
[/code]

次のようなノートが作成されるはずです。

<a href="https://rashita.net/blog/?attachment_id=23545" rel="attachment wp-att-23545"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-16.png" alt="" width="350" height="260" class="alignnone size-full wp-image-23545" /></a>

あるいはコードを次のようにかけば、チェック済みのチェックボックスが表示できます。

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with enml &quot;&lt;en-todo checked=\&quot;true\&quot;/&gt;this is Task&quot;
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=23547" rel="attachment wp-att-23547"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-18.png" alt="" width="353" height="253" class="alignnone size-full wp-image-23547" /></a>


簡単ですね。これを知っておくと、テンプレートからタスクリストを作る、といった用途に便利です。できれば、ENML contentの上書きや、ENMLでのappendが可能になって欲しいところですが、現状はできませんので、ノート内容の書き換えについてはHTML contentを使うしかありません。

その他、ENMLの情報については以下のページをどうぞ。

<a href="https://dev.evernote.com/doc/articles/enml.php" title="ENML - Evernote Developers">ENML - Evernote Developers/a>

<h2>Next Step</h2>

これで、AppleScriptでEvernoteを操作するための基本的な知識は一通り紹介できたかと思います。もちろん、細かい知識はまだまだ必要でしょうが、その辺はググればなんとかなります。あとはコードを書くだけです。

というわけで、次回は20回目なので、全体を振り返ってみるとしましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.16</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 49,103<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.16</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 184<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

