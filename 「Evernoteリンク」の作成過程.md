---
title : 「Evernoteリンク」の作成過程
link : 8321
date : Thu, 28 Jun 2012 01:00:36 +0000
categories : ["blogarts"]
tags : ["blog"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=8314">昨日のエントリー</a>で紹介した<a href="https://rashita.net/blog/?page_id=8276">Evernoteリンク</a>の作成方法について。

まず最初に考えたのは、「全ての記事を自分でチェックして、それをジャンル毎に分類し、リンクを貼っていく」というやり方。なかなか使い勝手の良いページができそうではありませんか。

しかし、あきらかに時間がかかりそうです。それに今後Evernoteについて書くたびに、そのページに修正を加えなければいけません。そうやって徐々に時間コストを積み上げていくのは、長期的な運用を前提とした場合あまり賢明な選択とはいえません。

すると、自動化です。

漠然と、Wordpressでphp書けばなんとかなるだろう、と考えました。

設置場所としては、こうした普通の更新ページよりも、固定ページの方がしっくりくるでしょう。作成すればヘッダーのリンクに自動的に追加されるのも魅力的です。

で、まず、固定ページのテンプレートを複数使い分けられるのかどうか。それが気になりました。

<a href="http://maruta.be/yumin/19" target="_blank"><img class="alignleft" align="left" border="0" src="http://capture.heartrails.com/150x130/shadow?http://maruta.be/yumin/19" alt="" width="150" height="130" /></a><a style="color:#0070C5;" href="http://maruta.be/yumin/19" target="_blank">ユミンのブログ | WordPressで複数の固定（テンプレート）ページを使用する方法</a><a href="http://b.hatena.ne.jp/entry/http://maruta.be/yumin/19" target="_blank"><img border="0" src="http://b.hatena.ne.jp/entry/image/http://maruta.be/yumin/19" alt="" /></a><br><strong>わかりやすい解説ありがとうございます。</strong><br style="clear:both;" /><br>

上の記事によると「可能」、とのこと。

PHPファイル作って、サーバーにアップすればOKのようです。とりあえず中の処理については考えずに、外殻だけのevernote.phpファイルを作成し、それをアップ。
※上のページで提示されているものをパクっただけのやつです。

どこにアップすればいいのか少し悩みましたが、「固定ページ」のテンプレートが入っているフォルダだろうとアタリを付けて、使用しているテーマのフォルダにアップ。

すると、無事認識された様子。

<a href="https://rashita.net/blog/wp-content/uploads/2012/06/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2012/06/screenshot2.png" alt="" title="screenshot" width="241" height="370" class="alignnone size-full wp-image-8325" /></a>

これで、固定ページのテンプレートが選択可能になりました。

<a href="https://rashita.net/blog/wp-content/uploads/2012/06/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2012/06/screenshot11.png" alt="" title="screenshot1" width="286" height="130" class="alignnone size-full wp-image-8326" /></a>

あとは、自分が想定するイメージのphpコードを書けばOK。

が、ここからずいぶん詰まりました。壁にぶつかりまくりです。

イメージとしてはEvernoteタグが付いた記事のタイトルを（リンクとして）縦にずらずらと並べたものを想定していました。get_posts()を使えばOKかなと思っていたんですが、どうにもうまくいきません。

「<a href="http://wpdocs.sourceforge.jp/%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%82%BF%E3%82%B0/get_posts">テンプレートタグ/get posts</a>」（WordPress Codex日本語版）

を見ても、タグの扱いが書いていません。もしかして、タグが使えない？

いろいろググり漁って、query_posts() ならタグが使えそうな感じ。
※「<a href="http://wpdocs.sourceforge.jp/%E3%83%86%E3%83%B3%E3%83%97%E3%83%AC%E3%83%BC%E3%83%88%E3%82%BF%E3%82%B0/query_posts">テンプレートタグ/query posts</a>」（WordPress Codex日本語版）

いろいろなサイトからコピペしてそれっぽいコードを作成。なんとか想定した表示ができました。

もしかしたら、本来的な使い方ではないのかもしれませんが、とりあえ表示ができたので個人的には満足です。

リンクを表示させている部分のコードはこんな感じ。

[php]
<ol reversed="reversed">
<?php query_posts('tag=evernote&posts_per_page=-1'); ?>
<?php if (have_posts()) : ?>
<?php while (have_posts()) : the_post(); ?>
	<div class="post" id="post-<?php the_ID(); ?>">
		<li><a href="<?php the_permalink() ?>" rel="bookmark" title="Permanent Link to <?php the_title(); ?>"><?php the_title(); ?></a></li></div>
	<?php endwhile; ?>
	<?php else : ?>
	<?php endif; ?>

	<?php wp_reset_query(); ?>
</ol>
[/php]


番号付きリストを作る＜ol＞のreversed属性は、番号を逆順にするもの。普通だと上から１、２、３、・・・となるのですが、これを指定すると、最後の要素から１、２、３、・・・と番号が上がってきます。ただ、ブラウザの対応は少ないようなので、普通に１から始まって見えているかもしれません。まあ害はないですね。

と、ここまで書いて気がついたんですが、最初の段階、つまりquery_posts()で拾ってくるときに、順番をひっくり返しておけば＜ol＞のナンバリングと記事のナンバリングが一致しますね。ただ、これだと最新記事にアクセスするときに、とんでもなく下までページを送らなければいけない事態が発生します。

うむむ。

まあ、新しい記事はブログのTopからアクセスしてもらうとして、リストは古いモノから新しいものに並べておくとしましょう。

なので、こんな感じです。

[php]

<ol>
<?php query_posts('tag=evernote&posts_per_page=-1&order=ASC'); ?>
<?php if (have_posts()) : ?>
<?php while (have_posts()) : the_post(); ?>
	<div class="post" id="post-<?php the_ID(); ?>">
		<li><a href="<?php the_permalink() ?>" rel="bookmark" title="Permanent Link to <?php the_title(); ?>"><?php the_title(); ?></a></li></div>
	<?php endwhile; ?>
	<?php else : ?>
	<?php endif; ?>

	<?php wp_reset_query(); ?>
</ol>

[/php]

という感じで出来たのが、「<a href="https://rashita.net/blog/?page_id=8276">Evernoteリンク</a>」です。昨日の時点では、上のコードでしたが、これを書いている間に下のバージョンに変更になりました。

同じことする人がいるかどうかはわかりませんが（きっといない）、とりあえず備忘録として。
<strong>
▼Coming Soon:</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/Evernote%E3%81%A8%E3%82%A2%E3%83%8A%E3%83%AD%E3%82%B0%E3%83%8E%E3%83%BC%E3%83%88%E3%81%AB%E3%82%88%E3%82%8B-%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E7%99%BA%E6%83%B3%E8%A1%93-%E3%83%87%E3%82%B8%E3%82%BF%E3%83%AB%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4774151505%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4774151505" target="_blank">Evernoteとアナログノートによる ハイブリッド発想術 (デジタル仕事術)</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/Evernote%E3%81%A8%E3%82%A2%E3%83%8A%E3%83%AD%E3%82%B0%E3%83%8E%E3%83%BC%E3%83%88%E3%81%AB%E3%82%88%E3%82%8B-%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E7%99%BA%E6%83%B3%E8%A1%93-%E3%83%87%E3%82%B8%E3%82%BF%E3%83%AB%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4774151505%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4774151505" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41XNAFAW1sL._SL160_.jpg" border="0" alt="Evernoteとアナログノートによる ハイブリッド発想術 (デジタル仕事術)" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />技術評論社  2012-06-30<br />売り上げランキング : 8929<br /><br /><br /><a href="http://www.amazon.co.jp/Evernote%E3%81%A8%E3%82%A2%E3%83%8A%E3%83%AD%E3%82%B0%E3%83%8E%E3%83%BC%E3%83%88%E3%81%AB%E3%82%88%E3%82%8B-%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E7%99%BA%E6%83%B3%E8%A1%93-%E3%83%87%E3%82%B8%E3%82%BF%E3%83%AB%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4774151505%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4774151505" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>
