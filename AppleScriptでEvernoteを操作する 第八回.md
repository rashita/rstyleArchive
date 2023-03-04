---
title : AppleScriptでEvernoteを操作する 第八回
link : 22933
date : Sat, 16 Sep 2017 02:32:19 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=22882">前回</a>は複数行の入力を可能とし、また入力されたテキストの一部だけを取り出すことを可能にしました。

今回は、これまで使用してきた create note 以外のコマンドを使い、ノートを操作してみましょう。

<h2>作成時に指定する</h2>

まず、普通にcreate note でノートを作成した場合、何も指定がなければノートブックはデフォルトのノートブックに放り込まれますし、またタグはつきません。逆に、create note で指定しておけば、特定のノートブックに入れたり、タグをつけたりが可能です。

たとえば、ノートブック指定は以下のようになります。

[code]
tell application &quot;Evernote&quot;
	create note title &quot;テストノート&quot; notebook &quot;002 [project/now-week]&quot; with text &quot;これはテストです&quot;
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=22935" rel="attachment wp-att-22935"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-45-500x108.png" alt="" width="500" height="108" class="alignnone size-medium wp-image-22935" /></a>

こうすると、デフォルトノートブックではなく、指定したノートブックにノートが作成されます。

<a href="https://rashita.net/blog/?attachment_id=22936" rel="attachment wp-att-22936"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-46.png" alt="" width="494" height="291" class="alignnone size-full wp-image-22936" /></a>


また、タグの場合は、以下のようになります。

[code]
tell application &quot;Evernote&quot;
	create note title &quot;テストノート&quot; tags &quot;Project&quot; with text &quot;これはテストです&quot;
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=22937" rel="attachment wp-att-22937"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-47.png" alt="" width="353" height="191" class="alignnone size-full wp-image-22937" /></a>

もし、一枚のノートに複数のタグをつけたい場合は、リストを使いましょう。

[code]
tell application &quot;Evernote&quot;
	create note title &quot;テストノート&quot; tags {&quot;Project&quot;, &quot;diary&quot;} with text &quot;これはテストです&quot;
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=22938" rel="attachment wp-att-22938"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-48.png" alt="" width="454" height="220" class="alignnone size-full wp-image-22938" /></a>

リストとは、{ }で囲まれた要素のことで、普通の変数が一つしか値を扱えないのに対し、リストは複数の値を扱うことができます。サンプルコードをご覧になればわかるように、要素同士は,で区切ればOKです。今回は二つのタグをつけましたが、三つでも四つでも同時に指定できます。

上記の二つを使えば、単にメモを保存するだけでなく、どこか特定のノートブックにメモを蓄積していったり、あるいはあるタグを常につけ続けることができるようになります。

もしリストについて詳しく知りたければ、以下のページを参照ください。

<a href="http://tonbi.jp/AppleScript/Tips/List/SetGroup.html">鳶嶋工房 / AppleScript / Tips / 値をリストでまとめる</a>

<h2>作成後の指定</h2>

さて、上記はノートの作成時にノートブックやタグを指定するものでした。しかし、何かしらの事情で、作成した後にノートブックやタグを指定したくなる場合もあるかもしれません。その際のやり方を少しだけ見ておきましょう。

まずは、ノートブックの変更から。

[code]
tell application &quot;Evernote&quot;
	set aNote to create note title &quot;テストノート&quot; with text &quot;これはテストです&quot;
	move aNote to notebook &quot;002 [project/now-week]&quot;
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=22939" rel="attachment wp-att-22939"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-49-500x160.png" alt="" width="500" height="160" class="alignnone size-medium wp-image-22939" /></a>

少しコードが変わっている点にご注意ください。これまでは単にcreate noteしていただけですが、今回のサンプルでは、その結果をaNoteという変数に指定しています。口語でこの命令を言い換えれば、「create noteコマンドでノートを作り、それをaNoteへ格納せよ」となります。

なぜ、こんなことをするのかというと、以降はこのaNoteを扱うことで、作成したノートに変更を加えられるようになるからです。もし、ノートを作成したままで放置してしまえば、それ以降の行で「あのノートのノートブックを変えてよ」と命令しようとしても、その「あのノート」がうまく指示できません。aNoteという変数を作りそこに放り込んでおくことで、簡単に「あのノート」が指定できるようになる、というわけです。この set ~ to  create note~ は非常によく使いますのでぜひとも覚えておいてください。

で、その後の行が本題です。moveコマンド。イメージする通り動かすためのコマンドです。上記のように書けば、ノートブック間の移動が可能となります。

では、タグはどうでしょうか。以下のように書きます。

[code]
tell application &quot;Evernote&quot;
	set aNote to create note title &quot;テストノート&quot; with text &quot;これはテストです&quot;
	assign tag &quot;Project&quot; to aNote
end tell
[/code]

<a href="https://rashita.net/blog/?attachment_id=22940" rel="attachment wp-att-22940"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-50-500x134.png" alt="" width="500" height="134" class="alignnone size-medium wp-image-22940" /></a>

タグの場合はassignコマンドを使用します。「Project」タグを、aNoteにアサインする、というようなイメージですね。

ちなみに、moveやassignコマンドなどを含むスクリプトのサンプルについては以下のページをご覧ください。

<a href="https://dev.evernote.com/doc/articles/applescript.php">Mac - Evernote Developers</a>

<h2>さいごに</h2>

これで、ノートのノートブックとタグがかなりいじれるようになってきました。使い方次第では、縦横無尽にノートを移動させられるでしょう。

次回はこの機能を使い、さらにメモアプリ・ノートアプリを強化してみます。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.16</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 38,081<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B0719S13KQ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51iRTqdvRnL._SL160_.jpg" alt="Evernoteとアナログノートによる　ハイブリッド発想術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B0719S13KQ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernoteとアナログノートによる　ハイブリッド発想術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.16</div></div><div class="amazlet-detail">技術評論社 (2017-05-29)<br />売り上げランキング: 116,830<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B0719S13KQ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.16</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 5,610<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


