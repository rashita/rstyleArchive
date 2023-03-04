---
title : AppleScriptでEvernoteを操作する 第十一回
link : 23106
date : Sat, 14 Oct 2017 02:14:39 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23059">前回</a>は、ifを使って、「Aという状況なら〜〜したいが、それ以外の状況なら○○したい」という条件分岐を導入しました。これで、「タグをつける場合」と「タグをつけない場合」の枝分かれが実現できたわけです。

今回はさらに複雑な枝分かれを実装してみましょう。

<h2>狙いとコード</h2>

前回では、"着想", "タスク", "資料", "タグなし"の四項目をリストで提示し、前三つに関してはタグをつけ、最後の一つについてはタグをつけない処理をしました。では、前三つはタグをつけ、しかも、そのうちの「資料」については、ノートブックを指定する、という処理ならどうでしょうか。もちろん、「タグなし」はこれまで通りタグをつけないとします。

少しまどろっこしいですが、たとえばこんな書き方ができます。

[code]
set taglist to {&quot;着想&quot;, &quot;タスク&quot;, &quot;資料&quot;, &quot;タグなし&quot;}

set myAnswer to display dialog &quot;メモの内容を入力してね！&quot; default answer &quot;&quot; &amp; return &amp; return &amp; return &amp; return
set memoTxt to text returned of myAnswer
set memoTitle to paragraph 1 of memoTxt

set applyTag to (choose from list taglist) as text

tell application &quot;Evernote&quot;
	
	if applyTag is equal to &quot;タグなし&quot; then
		create note title memoTitle with text memoTxt
	else if applyTag is equal to &quot;資料&quot; then
		create note title memoTitle notebook &quot;500 [スクラップ]&quot; tags applyTag with text memoTxt
	else
		create note title memoTitle tags applyTag with text memoTxt
	end if
	
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=23108" rel="attachment wp-att-23108"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-21-500x289.png" alt="" width="500" height="289" class="alignnone size-medium wp-image-23108" /></a>

注目したいのは、13行目のelse if applyTag is equal to "資料" thenです。前回はelse だけの構文を紹介しましたが、今回はそのあとにまたifが登場しています。これにより、「もしAの状況であれば、〜〜の処理をし、Bの状況であれば、○○し、そのどれでもなければ××し」という分岐が可能になっています。このelse if は複数接続可能なので、条件による分岐はいくらでも増やしていけます。


<h2>入れ子状の構造</h2>

あるいは、こういう書き方も可能です。

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
		if applyTag is equal to &quot;資料&quot; then
			create note title memoTitle notebook &quot;500 [スクラップ]&quot; tags applyTag with text memoTxt
		end if
		create note title memoTitle tags applyTag with text memoTxt
	end if
	
end tell
[/code]

今度はelseの後ろではなく、elseのブロックの中にif文が入っています。このようにif文は入れ子状にすることもできます。若干コードがわかりにくくなっているかもしれませんが、やっていることは、「もし〜だったら」を積み重ねているだけです。そして、これでかなり複雑な処理が書けるようになります。

たとえば、もし「タグなし」以外のものが選ばれたときは、さらにリストを示し、そこからノートブックを選んでもらって、それぞれのノートをそこに保存する、ということも可能になります。

if文とその条件式は、さまざまな書き方が可能ですので、上記が唯一の正解というわけではありません（むしろ冗長すぎるくらいです）。その辺は、実際にいろいろ書いて試してみてください。一例を挙げれば、最初の条件判断をapplyTag is equal to "タグなし" ではなく、applyTag is  not equal to "タグなし" として、「選ばれたタグが、〈タグなし〉でなかったら」というような書き方もできます。こう書くと、それ以降に続く処理も書き方が変わってきますね。こういうのを考えるのが好きな人はプログラミングに適正があるように思います。

<h2>next step</h2>

<del datetime="2017-10-21T02:37:25+00:00">さて、先ほども書いたとおり、else if は複数接続できるので、リストの項目一つごとに別の処理を割り当てることもできます。が数が多い場合は、else if else if else if ……と若干うっとうしさが増してしまうので、それとは違う式の書き方も覚えておきましょう。それについては次回紹介します。</del>

[2017年10月21日 11:38 追記 
うろ覚えで、case文があったような気がしたのですが、まったく全然存在しなかったのでこの話はここまでです。次回は別の切り口のツール作りについて書きます。]


<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.14</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 172,045<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.14</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 140<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
