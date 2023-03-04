---
title : AppleScriptでEvernoteを操作する 第十二回
link : 23138
date : Sat, 21 Oct 2017 02:50:06 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23106">前回</a>までは、ダイアログを表示し、ユーザーに入力してもらった内容で、新しいノートを作成する、というツールを作成していました。

今回は、視点を変えて、別の形に取り組んでみましょう。ユーザーに入力してもらった内容を、すでに存在するノートに書き加える、という形です。

<h2>狙いとコード</h2>

基本的な形は前回までの流れを引き継ぎます。ダイアログを出し、ユーザーに内容を入力してもらう。その結果を利用して、選択しているノートに追記する。コードは以下のようになります。

[code]
set myAnswer to display dialog &quot;メモの内容を入力してね！&quot; default answer &quot;&quot; &amp; return &amp; return &amp; return &amp; return
set memoTxt to text returned of myAnswer
set memoTitle to paragraph 1 of memoTxt

tell application &quot;Evernote&quot;

	set temp to selection
	append item 1 of temp text memoTxt
	
end tell
[/code]


<a href="https://rashita.net/blog/?attachment_id=23140" rel="attachment wp-att-23140"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-22-500x159.png" alt="" width="500" height="159" class="alignnone size-medium wp-image-23140" /></a>

※Evernoteで選択しているノート
<a href="https://rashita.net/blog/?attachment_id=23144" rel="attachment wp-att-23144"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-26-500x274.png" alt="" width="500" height="274" class="alignnone size-medium wp-image-23144" /></a>

※ツール起動後のダイアログで追記内容を入力
<a href="https://rashita.net/blog/?attachment_id=23145" rel="attachment wp-att-23145"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-27.png" alt="" width="420" height="224" class="alignnone size-medium wp-image-23145" /></a>

※ノートに追記された
<a href="https://rashita.net/blog/?attachment_id=23146" rel="attachment wp-att-23146"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-28-500x297.png" alt="" width="500" height="297" class="alignnone size-medium wp-image-23146" /></a>

コードの前半部分はこれまでと同じで、変わっているのは後半のEvernoteへの命令部分です。

まず7行目。「selection」というのは、「選択されているもの」というくらいの意味で、Evernoteであれば選択されたノートの情報が返ってきます。それをとりあえずtemp変数に保存。

次の行で、そのtempに対して、追記の命令を下しています。「append」がそれです。コマンドを読み下せば、「tempの1項目に、memoTxtの内容をtext形式で書き加えよ」となるでしょう。いろいろ新しい概念が出てきたのですが、とりあえずappendの解説からとりかかりましょう。構文的にはこうです。

append v ~

・vは対象となるノート
・~は書き込む内容

で使えるのは

・text 
・html 
・attachment 

の三種類。textはプレーンテキストで、htmlはhtmlタグの形式で追記ができ、attachmentはファイルの添付が可能です。

textとhtmlについてはどちらも文字列を指定するのですが、その違いはたとえば以下のようになります。

※入力は同じ
<a href="https://rashita.net/blog/?attachment_id=23141" rel="attachment wp-att-23141"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-23.png" alt="" width="435" height="226" class="alignnone size-full wp-image-23141" /></a>

※textで処理したもの
<a href="https://rashita.net/blog/?attachment_id=23142" rel="attachment wp-att-23142"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-24-500x72.png" alt="" width="500" height="72" class="alignnone size-medium wp-image-23142" /></a>

※htmlで処理したもの
<a href="https://rashita.net/blog/?attachment_id=23143" rel="attachment wp-att-23143"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-25-500x44.png" alt="" width="500" height="44" class="alignnone size-medium wp-image-23143" /></a>

もし文字を太字やリンクにしたければ、textではなくhtmlを使ってappendしましょう。ただしその場合、改行等がまるっと消えるので注意が必要です。

三つ目のattachmentは、少しややこしいので今回は割愛します。

<h3>item 1 of </h3>

もう一つ、覚えておきたいのが「item 1 of temp」という書き方です。

「item 1 of」とは、一つ目の項目という意味です。そして、tempには選択されているノートが入っているのでした。では、「item 1 of temp」とはなんでしょうか。もちろん「選択されているノートの一つ目の項目」ということです。これは、Evernote上でノートを複数選択できることを思い出していただければ納得できるでしょう。

上記のコードであれば、いくつノートを選択していても、その一番最初のノートに追記がなされます。無論一つしかノートが選択されていなければ、そのノートが一項目目です。

<h2>next step</h2>

この「append」という操作も、Evernoteでいろいろやる上では頻繁に登場します。ぜひとも覚えておいてください。また、選択したノートに対して操作を行うことも多いので、 selectionからノートを取り出す感覚にも慣れておきましょう。

とりあえず、今回は選択したノートの中の一つのノートに対して操作をしました。では、選択したノートすべてに操作を行う場合はどうでしょうか。それについては次回紹介します。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.21</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 180,221<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.21</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 129<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
