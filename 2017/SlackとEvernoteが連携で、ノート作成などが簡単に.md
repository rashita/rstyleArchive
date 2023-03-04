---
title : SlackとEvernoteが連携で、ノート作成などが簡単に
link : 23161
date : Tue, 24 Oct 2017 02:41:44 +0000
categories : ["evernoteの使い方"]
tags : ["evernote","slack"]
draft : false
author : 倉下忠憲
---

タイトル通りです。

<a href="https://blog.evernote.com/jp/2017/10/24/57814">Evernote × Slack 連携でアイデアを活用する 3 つの方法 - Evernote日本語版ブログ</a>

<blockquote>
すべてのアイデアを保管する場所が Evernote で、そのアイデアを他の人に共有するツールが Slack です。この 2 つのアプリがつながることで、情報を探す時間が減り、より多くの仕事を片付けられるはずです。
</blockquote>

設定などは以下のページから。

<a href="https://evernote.com/intl/jp/slack">Evernote と Slack を連携 | Evernote</a>

とりあえず、試してみましょう。

<h2>/noteコマンド</h2>

slack上で、/noteコマンドを入力。

<a href="https://rashita.net/blog/?attachment_id=23162" rel="attachment wp-att-23162"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-31-500x67.png" alt="" width="500" height="67" class="alignnone size-medium wp-image-23162" /></a>

Evernoteにコマンドが受容された模様。

<a href="https://rashita.net/blog/?attachment_id=23163" rel="attachment wp-att-23163"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-32-500x109.png" alt="" width="500" height="109" class="alignnone size-medium wp-image-23163" /></a>

Evernoteを覗いてみると、ノートが作成されていました。

<a href="https://rashita.net/blog/?attachment_id=23164" rel="attachment wp-att-23164"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-33-500x201.png" alt="" width="500" height="201" class="alignnone size-medium wp-image-23164" /></a>

では、さらに/noteでノートを作成したらどうなるか。

<a href="https://rashita.net/blog/?attachment_id=23165" rel="attachment wp-att-23165"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-34-500x71.png" alt="" width="500" height="71" class="alignnone size-medium wp-image-23165" /></a>

<a href="https://rashita.net/blog/?attachment_id=23166" rel="attachment wp-att-23166"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-35-500x234.png" alt="" width="500" height="234" class="alignnone size-medium wp-image-23166" /></a>

<a href="https://rashita.net/blog/?attachment_id=23167" rel="attachment wp-att-23167"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-36-500x235.png" alt="" width="500" height="235" class="alignnone size-medium wp-image-23167" /></a>

このように同一のノートに追記(append）される形になります。

では、別のチャネルで/noteすればどうなるか。

<a href="https://rashita.net/blog/?attachment_id=23168" rel="attachment wp-att-23168"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-37-500x574.png" alt="" width="500" height="574" class="alignnone size-medium wp-image-23168" /></a>

<a href="https://rashita.net/blog/?attachment_id=23169" rel="attachment wp-att-23169"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-38-500x254.png" alt="" width="500" height="254" class="alignnone size-medium wp-image-23169" /></a>

見事に同じノートに追記されます。ある種のプロジェクトに関する思いつきを一つのノートにまとめていく使い方になるでしょうか。

ちなみに、作成されたノート上部に表示されている説明は消してしまっても問題なさそうです。

<a href="https://rashita.net/blog/?attachment_id=23170" rel="attachment wp-att-23170"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-39-500x228.png" alt="" width="500" height="228" class="alignnone size-medium wp-image-23170" /></a>

ノートのタイトルを変えても大丈夫でした。

<a href="https://rashita.net/blog/?attachment_id=23171" rel="attachment wp-att-23171"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-40.png" alt="" width="443" height="324" class="alignnone size-full wp-image-23171" /></a>

おそらくやっていることは、一番最初にslack用ノートを作成し、そのインデックス(≒URL)を保持しておいて、以降はそのnoteに対してappendしていくというものでしょう。よって、ノート内容の編集、タグの添付、ノートブックの移動に関しては問題ありませんが、マージを行ってしまうとインデックスが変更されるので、新規ノートが作成されることになりそうです。

<h2>/clip</h2>

続いて、すでに送信されたメッセージなどをノート化する「/clip」コマンド。slack上で/clipを実行すれば、ヘルプが表示されます。

<a href="https://rashita.net/blog/?attachment_id=23172" rel="attachment wp-att-23172"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-41-500x254.png" alt="" width="500" height="254" class="alignnone size-medium wp-image-23172" /></a>

構文はこんな感じ。

[code]
/clip [starred] [since] &lt;message link or date&gt;
[/code]

/noteコマンドに比べるとややこしく見えますが、それほど難しくはありません。

基本は /clip &lt;message link or date&gt;の形で、/clip 2017 のように、クリップするデータ（日付）を指定します。データの指定方法は例えば、以下のようなものがあります。

june 1, 2017, december 2016, 2016, december, today, yesterday.

で、この/clipは、二つのオプションを持ちます。[starred]と [since]です。

starredをつけると、スターがついているメッセージだけがクリップされます。sinceをつけると、それ以降に続くdate（日付、URL）がクリップされます。この二つを同時に使うこともできます。

/clip yesterday  --昨日分をクリップ
/clip starred yesterday --昨日分のスター付きをクリップ
/clip since yesterday  --昨日からの分をクリップ
/clip starred since yesterday --昨日からの分のスター付きをクリップ

これらを組み合わせて、縦横無尽にEvernoteにノートを作成することが可能、というわけです。私の寂しい一人slcakで/clip 2016 を実行してみると、

<a href="https://rashita.net/blog/?attachment_id=23173" rel="attachment wp-att-23173"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-42-500x250.png" alt="" width="500" height="250" class="alignnone size-medium wp-image-23173" /></a>

こういう悲しいノートができました。全然使っていないことが丸わかりですね。でも、slack上でよくコミュニケーションしている人は、IFTTTを介さずにevernoteにクリップできるのは、なかなか便利かもしれません。

ちなみに、まったく同じ/clipコマンドを入力した場合でも、作成されるノートは別になる点が、/noteとの違いです。

<h2>/findコマンド</h2>

最後のコマンドが/find です。一応これも「/find」を実行すればヘルプが表示されますが、それほど難しいコマンドではありません。単に/find の後に、普段Evernoteで使っている検索文字列を入力すればOKです。

今回は、/find intitle:ss で実行してみました。「タイトルにssを含むもの」という意味です。コマンドが実行されると、検索結果が表示されます。

<a href="https://rashita.net/blog/?attachment_id=23174" rel="attachment wp-att-23174"><img src="https://rashita.net/blog/wp-content/uploads/2017/10/screenshot-43-500x427.png" alt="" width="500" height="427" class="alignnone size-medium wp-image-23174" /></a>


この画面は、他の参加者からは閲覧できませんのでご安心を。で、「Post here」ボタンを押すと、その内容がslackに投稿されます。ちなみに、長いnoteに関しては、Show moreで全文表示となります。

<h2>さいごに</h2>

基本的に一人で作業しているので、コミュニケーションツールとしてのSlackはあまり活躍していないのですが、/noteや/clipを使えば、業務日誌やプロジェクト日誌的に使えるのではないかな、という予感はあります。特に、/noteコマンドに関しては、一つのnoteに淡々とappendしていくメモツールが実は少ないので、そういう活躍の余地はあるでしょう。

後はまあ、バンバンSlack（とEvernote）を使っている人の報告を待ちましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.24</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 120<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.10.24</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 116,308<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
