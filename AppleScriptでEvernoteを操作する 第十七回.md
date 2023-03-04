---
title : AppleScriptでEvernoteを操作する 第十七回
link : 23461
date : Sat, 02 Dec 2017 02:06:48 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=23424" title="AppleScriptでEvernoteを操作する 第十六回 – R-style">前回</a>は、リストから、ユーザーにノートブックを選択してもらう処理を紹介しました。

今回は少し切り口を変えて、ノートの中身を操作する方法を紹介します。

<h2>狙いとコード</h2>

今回やることは、どれか一つのノートの中身を表示させることです。

まず一番シンプルな例でやってみましょう。自分でノートを作成し、そのノートの中身を表示させてみます。コードは以下のように書けます。

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with text &quot;this is sample note&quot;
	set anoteText to HTML content of anote
	display dialog anoteText
end tell
[/code]

コードを実行すると、以下のようなノートが作成されると共に、

<a href="https://rashita.net/blog/?attachment_id=23462" rel="attachment wp-att-23462"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-1.png" alt="" width="575" height="474" class="alignnone size-full wp-image-23462" /></a>

以下のようなダイアログが表示されるでしょう。

<a href="https://rashita.net/blog/?attachment_id=23463" rel="attachment wp-att-23463"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-2.png" alt="" width="433" height="161" class="alignnone size-full wp-image-23463" /></a>

やっていることはごくシンプルです。2行目で新規ノートを作成し、3行目でそのノートの中身を表示させています。ポイントは、 HTML content of anote の部分。対象のノートの中身をHTMLで取り出せ、というようなコマンドです。

作成されたノートと見比べてみるとわかりますが、たしかにダイアログで表示されているのはHTML要素です。ようするにEvernoteは、裏側でHTML的なものを使ってノートを処理している、ということですね。

で、実際それは、<a href="https://dev.evernote.com/doc/articles/enml.php" title="ENML - Evernote Developers">ENML</a>という拡張されたHTML（XHTML）なわけですが、そちらの方を取り出すこともできます。

先ほどのコードを、ごく微妙に書き換えてみましょう。

[code]
tell application &quot;Evernote&quot;
	set anote to create note title &quot;sample&quot; with text &quot;this is sample note&quot;
	set anoteText to ENML content of anote
	display dialog anoteText
end tell
[/code]

3行目の記述が多少変わっただけです。コードを実行すると、以下のようなダイアログが表示されるかと思います。

<a href="https://rashita.net/blog/?attachment_id=23464" rel="attachment wp-att-23464"><img src="https://rashita.net/blog/wp-content/uploads/2017/12/screenshot-3.png" alt="" width="414" height="184" class="alignnone size-full wp-image-23464" /></a>

明らかに記述量が増えていますね。そうです。どちらかと言えば、こちらが本体です。en-noteという独自のタグが出ていますが、これがHTMLおけるBodyタグのようなものと考えればよいでしょう（実際はmainタグが近い）。

ようするに、 HTML content of で取り出されるものは、en-noteタグの中身だけであり、しかもその中で使われているENML独自のタグなどもHTMLに変換されています。

よって扱いやすいのは明らかにHTML of content なのですが、ENML独自の要素を扱いたい場合は、 ENML content of を使うことになります。でもって、 ENML独自の要素の代表例がチェックボックスなのですが、その話はまた次回にしましょう。

<h2>Next Step</h2>

今回は、対象のノートの「中身」を取得する方法を紹介しました。

となると、次はそれを変更する方法となります。次回は、その方法を見ていきましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.02</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 90<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.12.02</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 112,964<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

