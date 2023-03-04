---
title : HTMLでEvernoteのノート・テンプレートを作る　第一回
link : 6327
date : Wed, 10 Aug 2011 03:53:41 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

個人的に最近はまっていることなんで、ちょっと足跡を残して置きます。
※HTML（CSS）に関する知識をお持ちの方にはまったく無用のエントリーです。

自分用のテンプレートを作れると、以下のようなノートが作れます。
※こんなマニアックなもの使わない、という方にも無用のエントリーです。

<a href="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot1.png" alt="screenshot1" title="screenshot1" width="444" height="336" class="alignnone size-full wp-image-6329" /></a>

<a href="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot3.png" alt="screenshot3" title="screenshot3" width="500" height="438" class="alignnone size-full wp-image-6331" /></a>

<a href="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot2.png" alt="screenshot2" title="screenshot2" width="500" height="300" class="alignnone size-full wp-image-6330" /></a>

<a href="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot.png"><img src="https://rashita.net/blog/wp-content/uploads/2011/08/screenshot.png" alt="screenshot" title="screenshot" width="500" height="430" class="alignnone size-full wp-image-6328" /></a>
<h3>概要</h3>
Evernoteはエディタ機能も（いちおう）存在しています。でもって、Webクリップも取り込める。

ということは、自分で気に入ったWebページを作り、それをクリッパーで取り込めば、自分用のフォーマットとして使えるということになります。

流れはごく簡単。

<ol>
	<li>テキストエディタか何かでHTMLファイルを作成する</li>
	<li>それをブラウザで表示させ</li>
	<li>さらにそれをクリップする</li>
</ol>



これだけです。作成したHTMLファイルをEvernoteに直接放り込む手段もありますが、Webクリップの方がなじみ深いと思うので、それをメインに解説します。

取り込んだノートは、原本として置いておき、それを必要に応じてコピーして使います。

<h4>作成環境</h4>
私の作成時の環境を書いておきます。特にWindowsだといろいろ違った結果になるかもしれませんので、あしからず。

<ul>
	<li>Mac OS X10.6.8</li>

	<li>Evernote(バージョン 3.0.0 Beta 3)</li>

	<li>Firefox 3.6.19</li>

	<li>CotEditor バージョン1.2</li>
</ul>



<h3>基本となるタグ</h3>
実際のウェブページを作るわけではないので、HTMLはごく基本的なものを押さえておけばそれでOKです。追加する要素は後回しにして、まず骨子になる部分を書きましょう。

<pre>
&lt;html&gt;
&lt;head&gt;
&lt;title&gt;ページのタイトル&lt;/title&gt;
&lt;/head&gt;
&lt;body&gt;
このへんが内容。
&lt;/body&gt;
&lt;/html&gt;
</pre>
</ol>

テキストエディタに上の文字を入力して、「test.html」という名前(名前は何でもよい）を保存すればそれでOK。そのファイルをウェブブラウザで見ればページとして表示されます。

Evernoteへのクリップでのポイントはページのタイトル部分。上のTitileというタグの後に来ている部分がそのページのタイトルになります。ウェブブラウザだとタブとかに表示されるやつですね。そのタイトルはEvernoteにクリップしたときにノートのタイトルになります。これはEvernote上で後から変更可能ですが、あらかじめ指定しておいた方が楽でしょう。

<h3>さいごに</h3>
これだけでは、テンプレートにほど遠いですが、とりあえず準備は整いました。

次回は、これに表組みを追加したり、色を付けたり、といった要素を紹介します。