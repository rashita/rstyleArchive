---
title : WordPressの固定ページテンプレートをいじって、Booksページをリニューアルしました
link : 12104
date : Mon, 09 Dec 2013 03:23:21 +0000
categories : ["blogarts"]
tags : ["blog"]
draft : false
author : 倉下忠憲
---

ブログ上部にあるメニューリンクに、「<a href="https://rashita.net/blog/?page_id=4342" target="_blank">Books</a>」という項目があります。

拙著の一覧を展開しているのですが、そこのデザインを変更しました。
※PC版の話なので、モバイル端末で閲覧されている方は「？」かもしれません。

リンクをクリックしてご覧いただくとわかりますが、ブログ記事のページとは若干デザインが違います。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot6.png" alt="screenshot" width="500" height="291" class="alignnone size-full wp-image-12105" /></a>

右側のサイドバーが消えていて、ワンカラムスタイルになっています。
<H3>オリジナルテンプレート作成の流れ</H3>WordPressの固定ページは、個別にテンプレートを指定できます。

たとえば、「<a href="https://rashita.net/blog/?page_id=8276" target="_blank">Evernoteリンク</a>」のページはそれ専用のテンプレートで作成されています。このテンプレートの作成方法は、

<a href="https://rashita.net/blog/?p=8321" target="_blank">「Evernoteリンク」の作成過程</a>

にて紹介しました。

オリジナルテンプレート作成の流れは、

<ol>
	<li>WordPressのテーマが保存されているフォルダにアクセス</li>
	<li>そこに新テンプレート用のphpファイルを作成</li>
	<li>固定ページ作成時に、そのテンプレートを選択</li>
</ol>

というものです。

新規でphpファイルを作成するのが手間な場合は、もともと存在している「page.php」（固定ページ用のデフォルトのテンプレート）をコピーして、そこに手を加える方法があります。

注意点は、ファイルの冒頭にテンプレート名の宣言を加えること。
[php] 
<?php
/*
Template Name: マイページ
*/
?>
[/php]
この「マイページ」にあたる部分が、テンプレート名になります。

phpのファイル名は「page2.php」とでもしておけば問題ありませんが、複数のテンプレートを作成する場合、どれがどれだったのかわかりにくくなるので、具体的な役割名を与えておいてもよいでしょう。（book.phpやevernote.phpなど）

<H3>追加されたか確認</H3>WordPress側できちんと認識されていれば、新規作成したphpファイルが、「外観→テーマの編集」のページに「固定ページテンプレート」として表示されます。もし表示されなければ、ファイルを保存している場所か、宣言の記述に問題があると思うので、確認してください。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot7.png" alt="screenshot" width="214" height="429" class="alignnone size-full wp-image-12106" /></a>

固定ページの新規作成でも、「book」が選択可能になっています。

<a href="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/12/screenshot8.png" alt="screenshot" width="294" height="441" class="alignnone size-full wp-image-12107" /></a>

<H3>新デザインについて</H3>今回使用した固定ページのテンプレートの一番大きなポイントは、
[php]
<?php get_sidebar(); ?>
[/php]

を削除したことです。というか、ほぼそれだけのために新規テンプレートを作ったようなものです。

ちなみにBooksページの下位にある、各書籍のページも同じテンプレートを使いました。既存のデザインと見比べてみると、やっぱり画像を使う場合は広いほうがいいですね。

蛇足ついでに書いておくと、デザインについては、「<a href="http://www.hyuki.com/" target="_blank">結城浩のホームページ</a>」からインスパイアを・・・というかほぼパクリですね。はい。

<H3>さいごに</H3>せっかくデザインを変えたということで、本を並べるだけでなく、それぞれの本にキャッチフレーズも付けてみました。ぜひご覧ください。個人的に、こういう作業は大好きです。

各書籍のページについては、まだ情報が不足しているものもあるので、じわじわ埋めていきたいと思います。

<strong>▼参考リンク：</strong>
<ul>
	<li><a href="http://wpdocs.sourceforge.jp/Pages_Add_New_SubPanel" target="_blank">Pages</a>(WordPress Codex 日本語版)</li>
	<li><a href="http://www.wapoo-custom.com/custom_manual/pagetemplate_krikae/" target="_blank">固定ページのテンプレートをページごとに切り替えるカスタム方法</a>（WordPressカスタム）</li>
	<li><a href="http://www.hyuki.com/" target="_blank">結城浩のホームページ</a></li>
</ul>

<strong>▼関連エントリー：</strong>
<ul>
	<li><a href="https://rashita.net/blog/?p=6043" target="_blank">WordPressのプラグインで過去記事へのランダムアクセスリンクを作ってみた</a></li>
	<li><a href="https://rashita.net/blog/?p=8314" target="_blank">R-styleに「Evernoteページ」を追加しました</a></li>
	<li><a href="https://rashita.net/blog/?p=8321" target="_blank">「Evernoteリンク」の作成過程</a></li>
</ul>


