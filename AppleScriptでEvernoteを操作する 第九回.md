---
title : AppleScriptでEvernoteを操作する 第九回
link : 22977
date : Sat, 23 Sep 2017 01:49:56 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=22933">前回</a>紹介した機能を使えば、メモアプリで作成するノートに常に「アイデア」というタグをつけたり、あるいはそのノートを「アイデアノート」ノートブックに常に入れておく、ということが可能となります。

それはそれで便利なのですが、常に同じ処理ではなく、選択肢（オプション）があった方が便利かもしれません。今回はその選択肢の作り方をみていきましょう。

<h2>４つのタグからの選択</h2>

目指すべき形は、次のようなものです。

まずアプリを立ち上げる。メモ入力画面が出てくるので、メモを入力する。OKボタンを押すと、次に選択肢が出てくる。そのうちどれかを選ぶと、選択肢に合わせたタグをつけてノートが作成される。

以上のような可変式メモアプリは、以下のようなコードで実装できます。

[code]
set taglist to {&quot;着想&quot;, &quot;タスク&quot;, &quot;資料&quot;, &quot;記録&quot;}

set myAnswer to display dialog &quot;メモの内容を入力してね！&quot; default answer &quot;&quot; &amp; return &amp; return &amp; return &amp; return
set memoTxt to text returned of myAnswer
set memoTitle to paragraph 1 of memoTxt

set applyTag to (choose from list taglist)

tell application &quot;Evernote&quot;
	create note title memoTitle tags applyTag with text memoTxt
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=22978" rel="attachment wp-att-22978"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-52-500x169.png" alt="" width="500" height="169" class="alignnone size-medium wp-image-22978" /></a>

コードを実行すると、お馴染みのダイアログが立ち上がり、

<a href="https://rashita.net/blog/?attachment_id=22979" rel="attachment wp-att-22979"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-53.png" alt="" width="412" height="223" class="alignnone size-medium wp-image-22979" /></a>

メモの内容を入力すると、次にリストが表示されます。ここでは、「タスク」を選択してみました。

<a href="https://rashita.net/blog/?attachment_id=22980" rel="attachment wp-att-22980"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-54.png" alt="" width="336" height="203" class="alignnone size-medium wp-image-22980" /></a>

OKボタンをプッシュすると、Evernoteにノートが作成され、先ほど選んだ「タスク」がタグとして設定されています。

<a href="https://rashita.net/blog/?attachment_id=22981" rel="attachment wp-att-22981"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-55.png" alt="" width="382" height="306" class="alignnone size-medium wp-image-22981" /></a>

上記のコードは、基本的にここまでの知見で組み立てられていますが、二つ新しい要素があります。一つは、 若干復習になりますが、set taglist to {"着想", "タスク", "資料", "記録"} の部分。{ }で要素を囲んだものは「リスト」と呼ばれるのでした。全体を{ }で囲み、要素を,で区切っていけばリストが作成できます。それをtaglistという変数に放り込んでいるのが、この行の役割です。以降の行では、taglistを扱うことで、このリストが操作できるわけです。

もう一つの新しい要素は、set applyTag to (choose from list taglist) の部分。ストレートに英語を読めば、taglistから選んで、その結果をapplyTagに放り込め、となりますが、おおよそその通りです。choose from list ~ は、~（リスト名）を表示させてそこからユーザーに選ばせろ、というコマンドで、簡易の選択において非常に便利に使えます。

あとは、その選択結果を保存しておき、それをそのままタグ名として利用してノートを作れば一件落着です。

<h2>next step</h2>

ただしこの場合、ノートには必ず何かしらのタグがつけられてしまいます。そういう用途なら別に構いませんが、タグをつけない、という選択肢も用意しておきたいところです。

ではたとえば、リストの中身を、 {"着想", "タスク", "資料", "タグなし"}とすればどうなるでしょうか。もちろんコードがそのままなら、「タグなし」というタグがノートにつくことになります。シュールですね。

うまくやるためには、状況に合わせたコードの分岐が必要でプログラミングでは「条件分岐」などと呼んだりします。その実装については、次回に譲りましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.23</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 66,390<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B0719S13KQ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51iRTqdvRnL._SL160_.jpg" alt="Evernoteとアナログノートによる　ハイブリッド発想術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B0719S13KQ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernoteとアナログノートによる　ハイブリッド発想術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.23</div></div><div class="amazlet-detail">技術評論社 (2017-05-29)<br />売り上げランキング: 130,607<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B0719S13KQ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.23</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 1,926<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

