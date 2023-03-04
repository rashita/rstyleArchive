---
title : AppleScriptでEvernoteを操作する 第四回
link : 22718
date : Sat, 19 Aug 2017 02:15:43 +0000
categories : ["evernoteの使い方"]
tags : ["applescrptでevernoteを操作する","applescript","evernote","〈学びの土曜日〉","スクリプトエディタ"]
draft : false
author : 倉下忠憲
---

では、<a href="https://rashita.net/blog/?p=22680">前回</a>紹介した create note コマンドをもう少し詳しくみていきましょう。

<a href="https://rashita.net/blog/?attachment_id=22684" rel="attachment wp-att-22684"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-9.png" alt="" width="426" height="151" class="alignnone size-full wp-image-22684" /></a>

<h2>create note</h2>

スクリプトエディタの「ライブラリ」で、create note コマンドを覗いてみます。

<a href="https://rashita.net/blog/?attachment_id=22720" rel="attachment wp-att-22720"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-15-500x201.png" alt="" width="500" height="201" class="alignnone size-medium wp-image-22720" /></a>

<blockquote>
create note v : Create a new note. You must specify exactly one of 'from file', 'from url', 'with text', or 'with html'.
</blockquote>

create noteコマンドは新しいノートを作るためのコマンドで、'from file', 'from url', 'with text', 'with html'のどれか一つを選んでね、と書かれています。前回使用したのは 'with text'で、おそらくこれが一番多く使われるでしょう。テキストの内容を使ってノートを作れ、ということです。

他のものも見ていきましょう。

<blockquote>
[from file file] : Clip the contents of the specified file.
[from url text] : Clip the contents of the specified URL.
[with text text] : Create a new note using the specified plain-text as content.
[with html text] : Create a new note using the specified html as content.
[with enml text] : Create a new note using the specified ENML as content. Do not include the <en-note> tags, only what should be between them.
</blockquote>

'from file'は、指定したファイルから、'from url'は、指定したURLからノートを作れ、となります。'with html'は、指定したHTMLで、'with enml'は、指定したENMLで、ということです。聞き慣れないENMLとは、Evernote専用のHTML（XHTML）だと考えてください。わからなければ、現時点ではスルーで結構です。

ようするに、上記はノートの中身を指定するための方法です。多くの場合は、普通のテキストで指定すればよいのですが、文字装飾やリンクを作りたいならHTMLが、チェックボックスなどを加えたいならENMLでの指定が必要となります。このあたりも、おいおい確認していくとして、create note コマンドの中身を引き続きみていきましょう。

<h2>メタ情報</h2>

<blockquote>
[title text] : Title for the new note.
[notebook text or notebook] : Notebook in which to place the note. Can be the name of a notebook or an object reference. If no notebook with the specified name exists a new one is created. If no notebook is specified, the default notebook for the account is used.
[tags list of text or list of tag] : Tags to assign to the new note. Can be the name of a tag or an object reference. If no tag with the specified name exists a new one is created.
[attachments list of file] : Files to attach to the note.
[created date] : Creation date for the new note. Defaults to now.
</blockquote>

こちらはオプション的要素であり、メタ情報を指定するために使います。必要なければ記述しなくても大丈夫です。

上記の中で頻繁に使われるのが'title text'で、ノートのタイトルを指定します。前回の例でも使用しました。その他、ノートブック、タグ、添付ファイル、作成日時を指定できます。

とは言え、これらすべてを暗記する必要はまったくありません。忘れたらこうして「ライブラリ」を確認すればいいだけですからね。ただ、頭の片隅にでも留めておくと、自分でスクリプトを設計するとき、「たしか、あんなことができたような……」とアイデアが閃きやすくなる効果はありますので、現時点では、なるほどこういう要素も指定できるのか、とざっと確認程度はしておいてください。

<h2>さいごに</h2>

とりあえず、簡単にまとめておきましょう。

create noteはノートを新規作成するためのコマンドであり、その内容は、テキスト、HTML(&ENML）、URL、ファイルから指定できる。またそのノートの、タイトル、ノートブック、タグ、添付ファイル、作成日時を指定することもできる。

以上です。

あとは、実際にコードを書いてその動作を確かめて見るとよいでしょう。

<code>tell application "Evernote"
	create note title "テスト" with text "テキストノートです"
end tell</code>

<code>tell application "Evernote"
	create note title "テスト" with html "<b>テキストノート</b>です"
end tell</code>

<code>tell application "Evernote"
	create note title "テスト" with enml "<en-todo/>テキストノートです"
end tell</code>

<code>tell application "Evernote"
	create note title "テスト" from url "https://rashita.net/blog/?p=22718"
end tell</code>

※ファイルからの作成は、また別のところで改めて。

これで create note の基本的な動作はOKです。次回はこのコマンドを使って、もう少しプログラミングらしくノートを作成してみるとしましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.19</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 134,036<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.19</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 2,494<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
