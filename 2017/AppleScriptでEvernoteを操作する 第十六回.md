---
title : AppleScriptでEvernoteを操作する 第十六回
link : 23424
date : Sat, 25 Nov 2017 00:38:06 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23357" title="AppleScriptでEvernoteを操作する 第十五回 – R-style">前回</a>は、あらかじめ作成しておいた選択肢から、ユーザーにノートブックを選んでもらうようにしました。

これはこれで便利なのですが、ときには存在するすべてのノートブックから選んでもらいたい場合もあるでしょう。その際、いちいちすべてのノートブック名を入力しておくのは不便ですし、そもそも大抵はどんなノートブックが入っているのかわからないので、これまでのやり方がまったく使えないこともあります。

どうすればいいのでしょうか。

<h2>狙いとコード</h2>

今回やることは簡単です。

全ノートブックのリストを表示し、そこからユーザーに選択してもらう。コードは以下のように書けます。

[code]
tell application &quot;Evernote&quot;
	set nlist to name of notebooks
	set selectNotebookName to choose from list nlist
	
	repeat with t in notebooks
		if (name of t) as text = (selectNotebookName) as text then
			set selectNotebook to t
			exit repaet
		end if
	end repeat
	
end tell
[/code]

tell application "Evernote"ブロックの中では、notebooksはEvernoteのノートブックの情報を持っています。それを参照すればよいわけですが、ここではそのうちのnameプロパティにアクセスしています。

2行目のコードは、簡単に言えば、nlistという変数に、全ノートブックの名前を入れてね、という命令です。

そして3行目で、そのリストからユーザーに選択してもらうダイアログを表示し、その結果をselectNotebookNameに保存します。

これで一件落着かというと、selectNotebookNameに入っているのはあくまで「ノートブックの名前」であって、ノートブックそのものの情報ではありません。ノートブックに対して何らかの操作を行う場合は、むしろその情報が必要となります。

そこで、selectNotebookNameに入っているノートブックの名前から、そのノートブックの情報を探します。他にもいろいろやり方はあるかと思いますが、ここで行っているのは、notebooksの中から一つひとつ要素（ノートブック情報）を取り出し、そのnamaと、selectNotebookNameを比較して、それが同じであれば、その取り出したノートブック（の情報）をselectNotebookに格納する、というものです。

イメージ的に言うならば、左手に商品名が書かれたラベルを持ち、箱の中から一つひとつ商品を取り出していって、ラベルと同じ商品名のものがあればそれを別の箱に入れて確保する、というようなことです。

ちなみに、もし適合するものがあれば、以降の比較作業は必要なくなるので、exit repaet によって繰り返しを抜けるようにしてあります。

前回の話と絡めれば、指定したノートブックから検索したい場合は、単にselectNotebookNameの情報を利用して、find notes コマンドを使えばOKです。選択したノートブックに対して操作する場合は、selectNotebookを使いましょう。

<h2>Next Step</h2>

これで、新規ノートの作成、ノート情報の取得、ノートの検索、ノートブック情報の扱いまでができるようになりました。省力化に関しては、これでかなりの部分がカバーできるでしょう。

次回は、ノートの中身情報の扱いについて見ていきます。


<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.11.25</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 202<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.11.25</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 210,843<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


