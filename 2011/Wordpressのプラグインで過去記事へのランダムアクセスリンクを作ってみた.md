---
title : Wordpressのプラグインで過去記事へのランダムアクセスリンクを作ってみた
link : 6043
date : Tue, 21 Jun 2011 02:54:39 +0000
categories : ["blogarts"]
tags : ["blog","wordpress"]
draft : false
author : 倉下忠憲
---

当R-styleは「毎日更新」を一つのルールにして、更新情報をTwitterに流しています。

ツイートはFacebook、FriendFeedにも流れるので、どれかで私をフォローしていただいている方にはその「更新情報」は届きます。もちろんRSSも公開していますので、リーダー系のアプリから確認することも可能です。

しかしながら、それらは基本的に「更新」されたものの情報です。過去に蓄積したエントリーは検索サイトからのアクセスルートはありますが、そうでないものは忘却の彼方へと置き去りになってしまいがちです。

そこで、「ランダムに過去記事にアクセスできる」環境を作ってみることにしました。Blogヘッダー部分にある「Random Link」をクリックしていただければ、無作為に過去記事にアクセスすることができます。

昔のブログ記事は相当酷いレベルの記事が多いのですが、お暇な時にでもポチっと押していたければ幸いです。

<h3>過去記事へのアクセス</h3>
では、このリンクの作り方の紹介・・・と行くまえにBlog過去記事へのリンク提供について少し書いておきます。

現状のこのブログでは、

<ul>
	<li>サイドバーの「最近の投稿」(Wordpress)</li>

	<li>サイドバーの「タグ・カテゴリー」(Wordpress)</li>

	<li>サイドバーの「はてブエントリー」（<a href="http://b.hatena.ne.jp/guide/blogparts.select?type=widget">ブログパーツ</a>）</li>
	<li>
記事末尾の「You might also like: 」（LinkWithinプラグイン使用）</li>
	<li>
記事末尾の「関連エントリー」（JRelatedプラグイン使用）</li>

	<li>記事末尾の「関連記事」（zenback使用）</li>

</ul>


という形で、過去記事へのリンクを出しています。

明らかに多いですね。特に記事末尾の「関連記事」は同じ機能のものが３つもあります。しかし、アルゴリズムが違うため提供されるリンクも異なっているので、現状は「まあいいか」と放置してあります。この関連記事はたまに自分で読み返しても新しい発見があったりするので、なかなか重宝しております。

これらは、近いテーマや興味のあるカテゴリーから記事を選択するもので、「偶然の出会い」はなかなか生まれません。Evernoteでも過去のものからランダムにノートが抽出されればかなり面白いと思いますが、その感覚で自分の記事にランダムアクセスしてみよう、という試みです。

同じようなことは、「Tweet Old Post」というプラグインでも実現できます。こちらは古い記事をランダムにTwitterに流すもの。最近「過去記事：〜」というつぶやきを見かけますが、あれを実現するプラグインです。こちらはアクセス数を上げるために使えるでしょう。

今回は、自分のBlogに「楽しめる要素」を追加したかっただけなので、「Customizable Post Listings」というプラグインを使い、「何が出てくるか分からない」リンクボタンを作成するだけにしておきました。
※ちなみにブログの更新情報をTwitterに流すのは「WordTwit」というプラグインを使っています。

<h3>Customizable Post Listings</h3>
「<a href="http://coffee2code.com/archives/2004/08/27/plugin-customizable-post-listings/">Customizable Post Listings</a>」は記事リンクを作成するプラグインです。最近の投稿を表示するのにも使えますが、今回の目的のようにランダムに記事を抽出するのにも使えます。

簡単な紹介は「<a href="http://f40.aaa.livedoor.jp/~benjamin/?p=366">ランダムに投稿記事を表示してくれるプラグイン</a>」をご覧いただければ、さっくりわかると思います。

Wordpressにプラグインをインストールして、ランダム記事を挿入したい場所に<code>
&lt;?php c2c_get_random_posts(1,'%post_URL%'); ?&gt;
</code>

を記入。これでOKです。コード中に含まれている「１」は記事数です。これを5とかにすれば5個の記事がランダムに抽出されます。

例えば、サイドバーにある「最近の投稿リスト」の代わりに「過去記事あれこれリスト」なども実現できますね。

<h4>URLとurlの違い</h4>
今回は、過去記事へのリンクではなく、過去記事へのURLだけが欲しかったので、"post_URL"ではなく、"post_url"を使っています。

post_URLだと、その記事のタイトルにリンクが付いたもの、小文字の方だと単にurlだけになります。記事タイトルが表示されてしまうと、「何が出てくるかわからない感」が減退してしまう上に、タイトルが長すぎるとヘッダーのデザインが大きく崩れるのであくまでリンク名は「Random Link」にしてあります。

コードはだいたいこんな感じ。上に書いてあることと基本的に同じです。ちょっと丁寧に書いただけ。


<pre><code>&lt;a href="&lt;?php c2c_get_random_posts($num_posts = 1,$format = "%post_url%"); ?
&gt;"&gt;Random Link&lt;/a&gt;
</code></pre>

これをテーマのヘッダーファイル（.php）に放り込んで終了、です。
<h3>さいごに</h3>
記事数が少ない間や、あるいは同じテーマで書き続けているブログの場合はそれほど必要無いかもしれませんが、ごっちゃに的なブログでは過去記事へのランダムアクセスというのも、なかなか面白い「機能」になるかもしれません。

興味ある方で、wordpressユーザーの方は、どうぞ。

<strong>▼参考記事：</strong>
<ul>
	<li><a href="http://coliss.com/articles/blog/wordpress/plugin/wordpress-plugin-tweet-old-post.html">古い記事をツイートして再利用できるWordPressのプラグイン -Tweet Old Post</a>（コリス）</li>

	<li><a href="http://wppluginsj.sourceforge.jp/wp-jrelated/">WordPress Related Post for Japanese (関連投稿表示プラグイン)</a>（WordPress Plugins/JSeries）</li>
	<li>
<a href="http://www.linkwithin.com/learn">LinkWithin</a></li>

	<li><a href="http://f40.aaa.livedoor.jp/~benjamin/?p=366">ランダムに投稿記事を表示してくれるプラグイン</a>（Tips Community）</li>

	<li><a href="http://coffee2code.com/archives/2004/08/27/plugin-customizable-post-listings/">Plugin: Customizable Post Listings</a>（coffee2code）</li>

	<li><a href="http://hsuzuki.ddo.jp/weblog/2372">プラグインCPLの操作マニュアル ver 2.0.1－PDF版</a>(Myblog)</li>
</ul>




<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4883377628/goodpic-22/" target="_top">Facebook×Twitterで実践するセルフブランディング</a></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4883377628/goodpic-22/" target="_top"><img src="http://ecx.images-amazon.com/images/I/51P3GCPM5wL._SL160_.jpg" border="0" alt="Facebook×Twitterで実践するセルフブランディング" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />ソシム  2011-05-30<br />売り上げランキング : 26297<br /><br /><br /><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4883377628/goodpic-22/" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4883377245/goodpic-22/" target="_top">WordPress レッスンブック 3.x対応</a></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4883377245/goodpic-22/" target="_top"><img src="http://ecx.images-amazon.com/images/I/51th9C%2B1nXL._SL160_.jpg" border="0" alt="WordPress レッスンブック 3.x対応" /></a></td><td valign="top"><font size="-1">エビスコム <br /><br />ソシム  2010-09-08<br />売り上げランキング : 1124<br /><br /><br /><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4883377245/goodpic-22/" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>


