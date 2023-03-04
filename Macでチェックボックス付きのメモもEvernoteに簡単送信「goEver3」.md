---
title : Macでチェックボックス付きのメモもEvernoteに簡単送信「goEver3」
link : 9642
date : Fri, 25 Jan 2013 07:18:53 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

Evernote for Macのアップデートが来ました。

<a href="http://blog.evernote.com/jp/2013/01/25/12169" target="_blank">Evernote for Mac アップデート: 検索機能、ショートカットおよびその他機能改善</a>（Evernote日本語ブログ）

いくつか注目の機能があるのですが、私が一番目を付けたのが

<blockquote>
高度な機能: AppleScript でチェックボックスが作成可能に
</blockquote>

の部分。

これまででもAppleScript経由でチェックボックス付きのノートを作成することは可能だったんですが、やや遠回りな手段を用いる必要がありました。

今回のバージョンからわりと簡単にできるみたいです。

というわけで、例のアプリをバージョンアップさせてみました。
<h3>goEver3</h3>
アプリを起動すると、次のようなダイアログが表示されます。

<a href="https://rashita.net/blog/wp-content/uploads/2013/01/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/01/screenshot6.png" alt="screenshot" width="474" height="391" class="alignnone size-full wp-image-9644" /></a>


メモしたいテキストを入力して送信ボタンをクリックすれば、それが即Evernoteに送られます。ここまではこれまでのバージョンと同じ。

新しく追加されたのが、真ん中のボタンです。「タスクで送信」を押すと、その名の通りチェックボックス付きのノートが出来上がります。

※こんな感じ
<a href="https://rashita.net/blog/wp-content/uploads/2013/01/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/01/screenshot11.png" alt="screenshot1" width="390" height="291" class="alignnone size-full wp-image-9645" /></a>

以上。

チェックボックスは1ノートに１つだけです。あと、5.0.5でないと「タスクで送信」はエラーがでると思われます。

<h3>さいごに</h3>
使いたい人がいるかはわかりませんが、一応アプリを公開しておきます。
→<a href="https://dl.dropbox.com/u/554861/goEver3.zip">こちらからどうぞ</a> 

ちなみに、コードはこんな感じ。

<script src="https://gist.github.com/4632325.js"></script>

さらなるバージョンアップとしては、改行ごとにチェックボックスを一つずつ追加する、ということになるでしょうか。まあ、個人的な需要はそれほど高くありませんので、気が向いたら作成してみます。

▼：その他リンクなど
<a href="https://rashita.net/blog/?p=6970" target="_blank">goEvernote（仮）をQuickSilverでもう一段早く&amp;改名しました</a>(R-style)
<a href="http://szk3s-scripts-in.tumblr.com/post/18995965555/everscribble" target="_blank">EverScribble - Evernoteにメモを書き散らすAppleScript</a>(
s_z_k_3's Scripts in Tumblr.com)
<a href="http://szk3s-scripts-in.tumblr.com/post/18592815768/appendcheckbox" target="_blank">Evernoteでノートにチェックボックスを追加するAppleScriptサブルーチン</a>(s_z_k_3's Scripts in Tumblr.com)
<a href="http://blog.goo.ne.jp/vallie/e/4dd9f978f29a3c2c68b92bd854e430aa" target="_blank">AppleScript : display dialog の表示と返り値</a>(GameSprit)
<a href="http://rashita.hatenablog.com/entry/2013/01/21/110828" target="_blank">Evernote for Mac 5.0.5beta でデイリータスクリストを作成するAppleScriptを書いた</a>(ジャムスタ)

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">EVERNOTE「超」知的生産術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51OnU0cd03L._SL160_.jpg" border="0" alt="EVERNOTE「超」知的生産術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2011-02-26<br />売り上げランキング : 9954<br /><br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E7%9F%A5%E7%9A%84%E7%94%9F%E7%94%A3%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540817%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540817" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

