---
title : AppleScriptでEvernoteを操作する 第七回
link : 22882
date : Sat, 09 Sep 2017 03:20:43 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=22828">前回</a>は、メモツールにノートタイトルを設定する機能をつけました。ユーザーに入力してもらう方法と、現在時刻を自動的に設定する方法です。

今回は、自動的に設定する方法で、かつ現在時刻を使わない方法にチャレンジしてみましょう。

<h2>すなわち一行目である</h2>

Evernoteへのメモ送信系アプリでよくあるのが、「メモの一行目をタイトルにしてしまう」という機能。これであれば、ユーザーの入力の手間も省けますし、タイトルでだいたい中身もわかります。

具体的には、

<a href="https://rashita.net/blog/?attachment_id=22883" rel="attachment wp-att-22883"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-27.png" alt="" width="464" height="281" class="alignnone size-full wp-image-22883" /></a>

こういう感じのメモを作れるようになればOKです。そのために、まず仕込みを一つ入れておきましょう。

<h2>複数行の入力</h2>

Display dialog は、普通に使うと、一行だけのテキストフィールドになります。リターンキーを押すと、そのままOKボタンが実行されて、一行しか入力できません。

<a href="https://rashita.net/blog/?attachment_id=22884" rel="attachment wp-att-22884"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-28.png" alt="" width="447" height="211" class="alignnone size-full wp-image-22884" /></a>

簡易のメモではこれでも構わないのですが、もう少し大きい入力をしたいときには不便です。そこで、Display dialog に少しアレンジを加えます。

といっても、大がかりなことではなく、

[code]
display dialog &quot;input &quot; default answer &quot;&quot; &amp; return
[/code]

<a href="https://rashita.net/blog/?attachment_id=22885" rel="attachment wp-att-22885"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-29.png" alt="" width="362" height="87" class="alignnone size-full wp-image-22885" /></a>

のように、最後に & returnを追加するだけです。すると、表示されるテキストフィールドが一行増えるだけなく、その下にも見えないなりに行が存在することになります。

<a href="https://rashita.net/blog/?attachment_id=22886" rel="attachment wp-att-22886"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-30.png" alt="" width="423" height="175" class="alignnone size-full wp-image-22886" /></a>

<a href="https://rashita.net/blog/?attachment_id=22887" rel="attachment wp-att-22887"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-31.png" alt="" width="429" height="179" class="alignnone size-medium wp-image-22887" /></a>

これで複数行の入力が可能となりました。見栄えがちょっと気になる方は、追加する& returnの数を増やしてもいいかもしれません。

<a href="https://rashita.net/blog/?attachment_id=22888" rel="attachment wp-att-22888"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-32-500x321.png" alt="" width="500" height="321" class="alignnone size-medium wp-image-22888" /></a>

& returnを増やした分だけ、表示されるフィールドの高さも増えます。このあたりは好みでどうぞ。

<h2>段落を取り出す</h2>

さて、あとは上記のダイアログを使い、ユーザーが入力したテキストの一行目だけを取り出して、それをノートのタイトルに使い、テキスト全体をノートの内容にすればOKです。たとえば、以下のように書けるでしょう。

[code]
set myAnswer to display dialog &quot;メモの内容を入力してね！&quot; default answer &quot;&quot; &amp; return &amp; return &amp; return &amp; return
set memoTxt to text returned of myAnswer
set memoTitle to paragraph 1 of memoTxt
 
tell application &quot;Evernote&quot;
    create note title memoTitle with text memoTxt
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=22889" rel="attachment wp-att-22889"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-33-500x239.png" alt="" width="500" height="239" class="alignnone size-medium wp-image-22889" /></a>

スクリプトを実行すれば、複数行のダイアログが立ち上がり、

<a href="https://rashita.net/blog/?attachment_id=22890" rel="attachment wp-att-22890"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-34.png" alt="" width="416" height="223" class="alignnone size-full wp-image-22890" /></a>

入力した内容から、一行目をタイトルにしたノートが作成されます。

<a href="https://rashita.net/blog/?attachment_id=22891" rel="attachment wp-att-22891"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-35.png" alt="" width="450" height="307" class="alignnone size-full wp-image-22891" /></a>

やっていることは極めて単純で、まず、memoTxtの中にユーザーが入力したテキストを保管し、その第一行目（第一パラグラフ）だけをmemoTitleに保管して、それぞれの変数を使ってノートを作成しています。

わかりやすくするために分割して書いていますが、この場合ならmemoTitleという変数を使わずに、memoTxt だけで、

[code]
tell application &quot;Evernote&quot;
    create note title (paragraph 1 of memoTxt) with text memoTxt
end tell
[/code]

のように書くこともできます。こちらは少し中級者向けかもしれませんので、わかりにくい場合は別々の変数で管理しておきましょう。

ちなみに、paragraph n of x で、xのn番目の段落を取り出す、となるわけですが、paragraph以外にもcharacter（文字）、word（単語）といった設定ができます。詳しくは以下のページをご覧ください。

<a href="http://www.12kai.com/scr/proptext.html">AppleScriptで文字列を処理する</a>

今はとりあえず、paragraph 1 of で一行目が取り出せるんだ、ということがわかっていればOKです。

さて、これで簡易のメモツールから、簡易のノート作成ツールにへと微妙にバージョンアップしました。次回はこのスクリプトをさらに変化させましょう。


<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.09</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 48,214<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.09</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 8,494<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
