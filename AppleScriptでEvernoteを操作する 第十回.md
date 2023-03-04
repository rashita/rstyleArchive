---
title : AppleScriptでEvernoteを操作する 第十回
link : 23059
date : Sat, 07 Oct 2017 00:23:55 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=22977">前回</a>は、タグを選択するダイアログを表示し、その結果に応じてノートにつけるタグを変える機能を追加しました。

今回は、そこに「タグをつけない」という選択を追加してみましょう。登場するのは条件分岐です。

<h2>狙いとコード</h2>

やりたいことは、ある選択においてはタグをつけ、別の選択においてはタグをつけない、という処理です。

そのような処理は、たとえば以下のように書けます。

[code]
set taglist to {&quot;着想&quot;, &quot;タスク&quot;, &quot;資料&quot;, &quot;タグなし&quot;}

set myAnswer to display dialog &quot;メモの内容を入力してね！&quot; default answer &quot;&quot; &amp; return &amp; return &amp; return &amp; return
set memoTxt to text returned of myAnswer
set memoTitle to paragraph 1 of memoTxt

set applyTag to (choose from list taglist) as text

tell application &quot;Evernote&quot;
	
	if applyTag is equal to &quot;タグなし&quot; then
		create note title memoTitle with text memoTxt
	else
		create note title memoTitle tags applyTag with text memoTxt
	end if
	
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=23062" rel="attachment wp-att-23062"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-9-500x267.png" alt="" width="500" height="267" class="alignnone size-medium wp-image-23062" /></a>

前回との違いは、まず選択肢の「記録」が「タグなし」になっていること。これはわかりやすく強調したもので、「記録」のままでも別に構いません。ともかくこの四番目の選択肢を選んだときだけは、他とは違いタグをつけないようにします。

次に、set applyTag to (choose from list taglist) as text　の行の最後にas text が追加されています。これはおまじないのようなものなのですが、意味としてはそのまま「テキストとして扱え！」となります。興味ある方はこのas textだけ削除してコードを動かしてみてください。

最後にノート作成の部分がややこしくなっています。重要なのは、 if applyTag is equal to "タグなし" then の箇所。これも英語をそのまま読めばOKで、「もし、applyTagの中身が、"タグなし"に等しいのであれば、」という意味で、その仮定（if）にマッチする場合のみ、下の行が実行されます。この場合は、create note title memoTitle with text memoTxt です。

さらにその次の行のelseは、「そうでなければ」となって、最初に提示した仮定にマッチしないのなら、その下の行が実行されます。そして最後のend if でこの仮定全体が終了します。

つまり、流れはこうです。まず最初にapplyTagの中身が"タグなし" が等しいかを確認する。等しければ create note title memoTitle with text memoTxtを実行し、等しくなければ create note title memoTitle tags applyTag with text memoTxtを実行する。この場合、二つの行の違いは、タグを当てているかどうかだけなので、結果もタグの有無の違いとして出てきます。

実際にコードを動かしてみると、

<a href="https://rashita.net/blog/?attachment_id=23063" rel="attachment wp-att-23063"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-10.png" alt="" width="411" height="211" class="alignnone size-full wp-image-23063" /></a>

<a href="https://rashita.net/blog/?attachment_id=23064" rel="attachment wp-att-23064"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-11.png" alt="" width="358" height="221" class="alignnone size-medium wp-image-23064" /></a>

<a href="https://rashita.net/blog/?attachment_id=23065" rel="attachment wp-att-23065"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-12.png" alt="" width="475" height="386" class="alignnone size-medium wp-image-23065" /></a>

無事タグのついていないノートを作成することができました。

<h2>仮定の書き方</h2>

条件分岐について書き始めるとキリがありませんので、詳しく知りたい方は以下のページをどうぞ。

<a href="http://tonbi.jp/AppleScript/Introduction/07/">鳶嶋工房 / AppleScript / 入門 / インテリジェントでいこう</a>

とりあえず押さえておきたいのは、今回使用した  is equal to は is や = に書き換えても同じ、という点。つまり、以下の書き方はどれも同様に機能します。

if applyTag is equal to "タグなし" then
if applyTag is  "タグなし" then
if applyTag =  "タグなし" then

自分にとってわかりやすい書き方を選んでください。

<h2>next step</h2>

このif文はディープであり、うまく使えるようになるとプログラミングの基本みたいなことはほとんどOKになるのですが、細かい話は多いので、必要に応じて紹介していくことにします。まずは、このシンプルな形を覚えてください。

次回は、このif文を使ってもう少し複雑な処理を導入してみます。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.07</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 126,144<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.07</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 100<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


