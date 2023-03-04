---
title : Evernoteに「未整理」タグつきでノートを作成するためのAppleScript
link : 26133
date : Fri, 09 Nov 2018 00:49:52 +0000
categories : ["evernoteの使い方"]
tags : ["applescript","evernote","メモ"]
draft : false
author : 倉下忠憲
---

先日、Evernoteの未整理タグ作戦を紹介しました。

<a href="https://rashita.net/blog/?p=26025">Evernoteの「未整理」タグで、タグづけを促進する – R-style</a>


問題は、これができるのがFastEverからであり、つまりはiPhoneからということです。できれば、Macを使っているときの緊急的なメモにも同じタグを付けたいところ。

そこで、AppleScriptです。

<a href="https://scrapbox.io/rashitamemo/Evernote%E3%81%AB%E3%80%8C%E6%9C%AA%E6%95%B4%E7%90%86%E3%80%8D%E3%82%BF%E3%82%B0%E3%81%A4%E3%81%8D%E3%81%A7%E3%83%8E%E3%83%BC%E3%83%88%E3%82%92%E4%BD%9C%E6%88%90%E3%81%99%E3%82%8B%E3%81%9F%E3%82%81%E3%81%AEAppleScript">Evernoteに「未整理」タグつきでノートを作成するためのAppleScript - 倉下忠憲の発想工房</a>

[code]
set myAnswer to display dialog &quot;please memo&quot; default answer &quot;&quot;
 set memoTxt to text returned of myAnswer
 set memoTitle to paragraph 1 of memoTxt
 
 tell application &quot;Evernote&quot;	
 	create note title memoTitle with text memoTxt tags &quot;未整理&quot;
 end tell
[/code]

このスクリプトを実行すると、以下のダイアログが立ち上がり、

<a href="https://rashita.net/blog/?attachment_id=26134" rel="attachment wp-att-26134"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-44.png" alt="" width="853" height="484" class="alignnone size-full wp-image-26134" /></a>

何か適当に入力して、OKボタンを押せば、

<a href="https://rashita.net/blog/?attachment_id=26135" rel="attachment wp-att-26135"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-45.png" alt="" width="639" height="425" class="alignnone size-full wp-image-26135" /></a>

以上のようなノートが作成されます。

もし「未整理」ではなく「未処理」がよい、といった場合は、コードの中のtags "未整理"の部分を書き換えてください。

これをもう少し改良すれば、「タグなし」「未整理タグをつける」「何か別のタグをつける」みたいなパターンから選べるようにもできるでしょう。あと、Evernoteでノートを作りつつ、Scrapboxに新規ページを作成する、というのも可能なはずです（URLを開けばいいだけだから）。その辺はご自由にどうぞ。

とりあえず、最近はタグを結構重視しているので、もし同じようにお使いならばこのコードも参考にどうぞ。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.11.09</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 313<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01EL08HW2/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51i02uyvjAL._SL160_.jpg" alt="EVERNOTE「超」知的生産術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01EL08HW2/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">EVERNOTE「超」知的生産術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.11.09</div></div><div class="amazlet-detail">C＆R研究所 (2016-04-21)<br />売り上げランキング: 34,108<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01EL08HW2/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

