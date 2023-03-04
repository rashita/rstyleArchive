---
title : AppleScriptでEvernoteを操作する 第十三回
link : 23208
date : Sat, 28 Oct 2017 03:01:58 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23138">前回</a>は、選択したノートに対して追記する動作を確認しました。使ったコマンドは、appendですね。

その際、動作の対象になったのは単一のノートでした。「選択されたノート」からitem of 1で取り出せば、ただ一つだけのノートを対象とできます。

では、複数のノートを処理したい場合はどうすればよいのでしょうか。今回は、それを紹介します。

<h2>狙いとコード</h2>

たとえば、選択したノートすべてに対して、ノートタイトルの変更を行う場合を考えてみましょう。いくつかのノートがあり、それらのノートのタイトルに対して【日報】という文字を付け加えます。

コードはたとえば次のような書き方ができるでしょう。

[code]
tell application &quot;Evernote&quot;
	
	set temp to selection
	repeat with a in temp
		set title of a to &quot;【日報】&quot; &amp; title of a
	end repeat
	
end tell
[/code]
<a href="https://rashita.net/blog/?attachment_id=23210" rel="attachment wp-att-23210"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-45.png" alt="" width="337" height="231" class="alignnone size-full wp-image-23210" /></a>

まず選択しているノートの情報を変数tempに放り込みます。ここまでは前回と同じ。前回ではそこからitem of 1で一つだけのノートを取り出だしていましたが、今回はrepeat inを使っています。

repeat with a in temp

で、「tempに入っているものを頭から一つずつ取り出していき、変数aに入れていく」という命令になります。その意味は、次の行を見ればよりはっきりするでしょう。

set title of a to "【日報】" & title of a は、一見ややこしいですが、set ○○ to ▽▽の形を思い出してもらえば簡単でしょう。title of a の中身を、title of aの中身に【日報】を加えたものに置き換える、ということです。その実行例が、以下です。

<a href="https://rashita.net/blog/?attachment_id=23211" rel="attachment wp-att-23211"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-46.png" alt="" width="1051" height="296" class="alignnone size-full wp-image-23211" /></a>

<a href="https://rashita.net/blog/?attachment_id=23212" rel="attachment wp-att-23212"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-47.png" alt="" width="1114" height="212" class="alignnone size-full wp-image-23212" /></a>

つまり、以下の文は、

repeat with a in temp
　set title of a to "【日報】" & title of a
end repeat

仮にtempの中に3つのノート（ノートX、ノートY、ノートZ）が入っているとすれば、	

set title of ノートX to "【日報】" & title of ノートX
set title of ノートY to "【日報】" & title of ノートY
set title of ノートZ to "【日報】" & title of ノートZ

が実行される、ということです。これがrepaet文がもたらす繰り返しの効果です。

<h2>next step</h2>

繰り返しもまた、プログラミングで頻繁に登場する要素なので覚えて置いてください。特にこの「選択したノートすべてに対して処理を行う」というのは、ちょっとした処理を行う際にも便利となります。今回のようにノートタイトルを書き換えたり、一定の要素を追記したりといったことが、ごく短いコードだけで実現できるので、たいへんな省力化となります。

AppleScriptにおける、その他のrepeatの使い方については、以下のページが参考になりますので、気になる方は目を通しておいてください。

<a href="http://tonbi.jp/AppleScript/Introduction/08/">鳶嶋工房 / AppleScript / 入門 / 繰り返しで処理しよう</a>

次回は、選択されたノート以外のノート情報の取得について見ていきましょう。