---
title : AppleScriptでEvernoteを操作する 第十四回
link : 23303
date : Sat, 11 Nov 2017 02:31:24 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23208" target="_blank">前回</a>は、選択されたノートの複数を対象とした処理について書きました。これを使えば、ノートタイトルの一括処理などが簡単に行えますね。

今回は、「選択されたノート」以外によるノートの処理方法を紹介してみます。使うのは、検索です。

<h2>狙いとコード</h2>

たとえば、特定のノートブックの中にあるノートについて処理したい、としましょう。

そのためには、その「特定のノートブックの中にあるノート」の情報を取得しなければならないわけですが、そういうときには、 <strong>find notes</strong> コマンドが使えます。その名の通り、ノートを見つけ出すための命令です。

書き方は、

find notes v

で、vには、Evernoteで使う検索構文を入れます。普通にキーワードを入れてもいいですし、notebook:~や、tag:~のようにノートブックやタグを指定することもできます。使える構文については以下のページを参照してみてください。

<a href="https://help.evernote.com/hc/ja/articles/208313828-Evernote-%E3%81%AE%E9%AB%98%E5%BA%A6%E3%81%AA%E6%A4%9C%E7%B4%A2%E6%A7%8B%E6%96%87%E3%81%AE%E4%BD%BF%E3%81%84%E6%96%B9" target="_blank">Evernote の高度な検索構文の使い方 – Evernote ヘルプ＆参考情報</a>

今回は、inboxノートブックに入っているノートに対して、何かしらの操作を行うとしましょう。コードは以下のように書けます。

[code]
set targetNotebook to &quot;001 [inbox]&quot;

tell application &quot;Evernote&quot;
	
	set resultNote to find notes &quot;notebook:\&quot;&quot; &amp; targetNotebook &amp; &quot;\&quot;&quot;
	repeat with i in resultNote
		log i
	end repeat

end tell
[/code]
<a href="https://rashita.net/blog/?attachment_id=23305" rel="attachment wp-att-23305"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-21.png" alt="" width="465" height="233" class="alignnone size-full wp-image-23305" /></a>
まず、探したいノートブックの名前を変数targetNotebooに入れておきます。私のinboxは、「001 [inbox]」という名前になっているので、それをそのままコピペしました。

続いてEvernoteへの命令です。５行目に先ほど紹介した、find notes コマンドが出ていますね。書き方がややこしいので詳しく解説しますが、その前にこの文全体について書いておきましょう。

この文では、find notesによる検索で見つかったノートの情報を変数resultNoteに入れるように指定しています。以降は、この resultNote を扱えば、それらのノートが操作できます。そういう文です。

では、5行目をもう少し詳しくみていきましょう。find notesの後に以下のような記述が続きます。

"notebook:\"" & targetNotebook & "\""

記号が多くてややこしいですが、これをEvernoteの検索文風に書けば以下になります。

notebook:"001 [inbox]"

こういう書き方なら、お馴染みでしょう。今回は001 [inbox]の部分がtargetNotebookに置き換えられているのですが、一筋縄ではいかないのが " という記号です。コード内では、""で囲まれた部分が「文字列ですよ」ということになるのですが、それはEvernoteの検索構文でも同様です。つまり、以下のように書くとうまくいきません。

 find notes "notebook:"001 [inbox]""
 
この場合は、"notebook:"までが一つの文字列だと判断されてスクリプトがうまく動きません。逆に、以下のように書くと、
 
find notes "notebook:001 [inbox]"

今度はEvernoteでの検索が期待しないものになります。そこで出てくるのが、エスケープ文字なのですが、簡単に言えば、""で括った中で、"を使いたいなら、そのことを明示してね、ということです。で、その明示に使われるのが  \ という記号です。この\の後に続く"は、日本語的に言えば、「」つきで扱われます。特別な意味を持つ（あるいは特別な意味を持たない）記号として扱われるのです。

そのことを踏まえて再び5行を見返せば、

"notebook:\"" & targetNotebook & "\""

は、&──これは文字列を足し算してくれます──を使った３つのブロックで構成されており、最初のブロックは、notebook:" までを 二つ目のブロックは、 001 [inbox] までを、最後のブロックでは " を担当していることがわかります。それらを結合すると、

notebook:"001 [inbox]"

となるわけですね。ちなみに、targetNotebookの中身を、

set targetNotebook to "\"001 [inbox]\""

としておけば、5行目は次のようになります。
 
set resultNote to find notes "notebook:" & targetNotebook
 
あらかじめ探すノートブックが決まっている場合はこちらの書き方がシンプルですが、もしユーザーにテキストを入力してもらって、その値を使って探す、という場合は最初の書き方の方がおそらくはよいでしょう。

<h2>next step</h2>

あとは前回と同じで、resultNoteに格納されたノートの情報を、repeatを使って一つずつ取り出し、それに対して処理していけばいいことになります。

リピートでノート情報が格納されるiに対して、ifで判断してけば、「〜〜ノートブックにある、~~というタイトルのノートに対しては○○の処理を行う」といったことも可能です。

次回はこのfind notes を使った、もう少し柔軟性のある検索をやってみましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.11.11</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 218,172<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.11.11</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 477<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

