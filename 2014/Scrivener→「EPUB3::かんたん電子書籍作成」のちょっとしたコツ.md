---
title : Scrivener→「EPUB3::かんたん電子書籍作成」のちょっとしたコツ
link : 12662
date : Wed, 12 Feb 2014 02:39:08 +0000
categories : ["scrivenerへの散歩道","物書き生活と道具箱"]
tags : ["scrivener","電子書籍"]
draft : false
author : 倉下忠憲
---

拙著新刊でも紹介した、以下のWebツール。

<a href="http://books.doncha.net/epub/" target="_blank">doncha.net EPUB3::かんたん電子書籍作成</a>

本当に、とても簡単にEPUB３ファイルを作成してくれます。

注意点は、章タイトル部分に「（小見出し）」を入れることぐらいでしょうか。これがページの区切りとしての機能してくれます。

技術的に難しい話はなく、単に区切りになる箇所にコピペしていくだけです。が、大きなファイルだと、やや面倒かもしれません。

<H3>Scrivenerのフォーマット機能</H3>私はScrivenerで（大がかりな）ドキュメントを作成・管理しております。

<h2><span style="color: rgb(0, 0, 255);">Scrivener</span></h2><div style="margin: 0;float: left;"><div style="margin-left: 109px;"><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" rel="nofollow" style="text-decoration: none;"><img src="http://a375.phobos.apple.com/us/r1000/068/Purple/v4/7f/c7/66/7fc7663d-0b33-0fcb-7924-d384ce39b2a5/Scrivener.100x100-75.png" style="margin-left: -109px; float: left; width: 100px; height: 100px;"><img src="http://r.mzstatic.com/htmlResources/2338/images/mask100.png" style="margin-left: -109px; float: left; width: 100px; height: 100px;" /></a></div></div> カテゴリ: 仕事効率化, 教育<br><br> 販売元: <a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" rel="nofollow">Literature & Latte - Literature & Latte Ltd</a><br> リリース日: 2011/07/06<br style="clear: both;">

このツール、紹介しきれないぐらい高機能なのですが、ある機能を使うと簡単に「（小見出し）」を追加していくことができます。

たとえば、こういうシンプルな構成のファイル。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot5.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot5.png" alt="screenshot" width="360" height="376" class="alignnone size-full wp-image-12663" /></a>

11個の原稿が入っており、それぞれが一つの章に相当します。画像の右側をご覧いただければわかりますが、本文中にタイトルや見出しは入っていません。

で、このファイルを「Compile」する際に、一工夫いれてみます。

「Compile for」 をtxt（プレーンテキスト）に選択し、サイドバーの「Formatting」クリック。原稿ファイルが入っている階層を選択。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot10.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot10.png" alt="screenshot" width="500" height="340" class="alignnone size-full wp-image-12669" /></a>

その後、TitleのチェックボックスをOnにします。こうすると、自動的に「原稿のタイトル」が本文中に挿入されます。この場合、「原稿のタイトル」とはBinderに表示されているファイル名のことです。

さらに「Section Layout…」をクリック。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot6.png" alt="screenshot" width="382" height="347" class="alignnone size-full wp-image-12664" /></a>

こんな画面が出てきます。

Prefixは接頭辞、Suffixは接尾辞です。タイトルの前、後ろに何か付けますか？というダイアログです。これを使うと章番号を自動的に割り振ることもできるのですが、今回の目的はそれではありません。

このPrefixに「（小見出し）」を入力して、「OK」。

これだけです。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot7.png" alt="screenshot" width="451" height="292" class="alignnone size-full wp-image-12665" /></a>
※下のサンプルが変化しています。

早速Compile（コンパイル）してみると、出力されたテキストファイルはこうなりました。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot8.png" alt="screenshot" width="500" height="240" class="alignnone size-full wp-image-12666" /></a>

きちんと「（小見出し）」が入っていますね。当然、これに続く10の原稿のタイトル部分にも「（小見出し）」が入っています。

それを<a href="http://books.doncha.net/epub/" target="_blank">doncha.net EPUB3::かんたん電子書籍作成</a>に通して、iBooksで確認してみしょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot9.png" alt="screenshot" width="500" height="700" class="alignnone size-full wp-image-12667" /></a>

きちんと表示されております。目次をのぞいてみると、

<a href="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/02/screenshot11.png" alt="screenshot" width="397" height="559" class="alignnone size-full wp-image-12671" /></a>

完璧ですね。

<H3>さいごに</H3>Scrivenerでは、元の原稿の中身は変えずに、（小見出し）を付けてコンパイルしたり、あるいは別の接頭辞を付けてコンパイルしたりと自由自在にコントロール可能です。

さらに、階層構造を操作すれば、一つのファイル内でも（小見出し）を付ける箇所、付けない箇所を操作できます。

いやはや便利ですね。

<strong>▼告知:</strong>
2月17日に、八重洲ブックセンターさんで以下の新刊に関するブックセミナーを行います。

電子書籍の最初の一歩を踏み出せていない方はぜひご来場ください。参加料は無料ですが、事前に登録が必要ですのでご注意ください。

<a href="http://www.yaesu-book.co.jp/events/talk/2919/" target="_blank">倉下忠憲さん講演会　「セルフ・パブリッシングの最初の一歩」</a>

<a href="https://rashita.net/blog/?p=12536" target="_blank">[告知] 2月17日に八重洲ブックセンター本店さんで新刊イベントを行います</a>

