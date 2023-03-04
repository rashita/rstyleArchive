---
title : AppleScriptでEvernoteを操作する 第十五回
link : 23357
date : Fri, 17 Nov 2017 22:00:20 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---



<a href="https://rashita.net/blog/?p=23303" title="AppleScriptでEvernoteを操作する 第十四回 – R-style">前回</a>は、検索を使ってノートの情報を取得してみました。キーワードを指定することで、ノートブックやタグを限定することも可能です。

ただし、前回では検索キーワードは固定されていました。それを選択できるようにするのは、どうすればいいでしょうか。

<h2>狙いとコード</h2>

前回では、あらかじめ検索するノートブックの名前をコードに埋め込んでいました。だから、コードを何度実行しても同じノートブックが検索されます。では、それに柔軟性を持たせるにはどうすればいいでしょうか。

<ul>
<li>複数のノートブックの選択肢を用意しておき、そこから選んでもらう</li>
<li>ノートブックリストの一覧を表示し、そこから選んでもらう</li>
<li>ユーザーにノートブック名を入力してもらう</li>
</ul>

上記の三つが考えられますが、三番目については「ユーザーがノートブックの名前を正確に覚えている」という前提が必要で、その前提は来年日本から大型の油田が発見される程度には望み薄なので避けておいた方がよいでしょう。というわけで、今回はまず一つ目の方法でやってみます。

コードは以下のようになります。

[code]
set targetNotebookList to {&quot;001 [inbox]&quot;, &quot;002 [project/now-week]&quot;, &quot;003 [day/stock]&quot;}
set targetNotebook to (choose from list targetNotebookList) as text

tell application &quot;Evernote&quot;
	
	set resultNote to find notes &quot;notebook:\&quot;&quot; &amp; targetNotebook &amp; &quot;\&quot;&quot;
	repeat with i in resultNote
		--ノートに対する処理をここに書く
	end repeat
	
end tell
[/code]
<a href="https://rashita.net/blog/?attachment_id=23358" rel="attachment wp-att-23358"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-26.png" alt="" width="582" height="232" class="alignnone size-full wp-image-23358" /></a>

簡単ですね。まず選択肢として上げたいノートブック名をリスト（配列）で指定しておき、あとはそのリストからユーザーに選んでもらい、その答えを使ってfind notesを走らせる、というものです。

これを少しアレンジすれば、ノートブックを選択してもらい、さらに検索のキーワードも入力してもらう、なんてこともできます。つまり「〜〜ノートブックから▼▼▼というキーワードが入ったノートを探す」というようなことですね。

コードとしては以下です。

[code]

set targetNotebookList to {&quot;001 [inbox]&quot;, &quot;002 [project/now-week]&quot;, &quot;003 [day/stock]&quot;}
set targetNotebook to (choose from list targetNotebookList) as text

set myAnswer to display dialog &quot;検索のキーワードを入力してね！&quot; default answer &quot;&quot;
set memoTxt to text returned of myAnswer


tell application &quot;Evernote&quot;
	
	set resultNote to find notes &quot;notebook:\&quot;&quot; &amp; targetNotebook &amp; &quot;\&quot; &quot; &amp; memoTxt
	repeat with i in resultNote
		--ノートに対する処理をここに書く
	end repeat
	
end tell

[/code]

これも難しくありません。ここまで紹介してきた知識で書けます。ダイアログを表示し、ユーザーに入力してもらったテキストを使い、find notesを走らせる。これだけです。

ただし、この場合、キーワードによってはノートが一つも見つからないこともあり、そうしたときに別の処理を行いたいなら以下のように書けます。

[code]
set targetNotebookList to {&quot;001 [inbox]&quot;, &quot;002 [project/now-week]&quot;, &quot;003 [day/stock]&quot;}
set targetNotebook to (choose from list targetNotebookList) as text

set myAnswer to display dialog &quot;検索のキーワードを入力してね！&quot; default answer &quot;&quot;
set memoTxt to text returned of myAnswer

tell application &quot;Evernote&quot;
	
	set resultNote to find notes &quot;notebook:\&quot;&quot; &amp; targetNotebook &amp; &quot;\&quot; &quot; &amp; memoTxt
	if length of resultNote ≥ 1 then
		repeat with i in resultNote
			--ノートに対する処理をここに書く
		end repeat
	else
		display dialog &quot;ノートはありません&quot;
	end if
	
end tell
[/code]

途中までは同じで、ノートの処理に入る前にif文が一つ追加されています。 length of resultNote は resultNoteに入っている要素の数を返すもので、それが１よりも大きいならノートの処理を行い、そうでなければ別の処理を行う、という進行になっています。

<h2>Next Step</h2>

だんだんと新しい知識を使わなくてもコードが書けるようになってきました。こうなってくると俄然プログラミングは楽しくなってきます。

さて、今回はあらかじめノートブックのリストを設定していましたが、そのとき存在するすべてのノートブックから選んで欲しいときはどうすればよいでしょうか。それについては次回に。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.11.17</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 288<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.11.17</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 135,855<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
