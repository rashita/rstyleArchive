---
title : WordpressでのEvernoteのサイトメモリー導入について
link : 4545
date : Thu, 16 Sep 2010 04:20:05 +0000
categories : ["物書き生活と道具箱"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

以前簡単に紹介しまたが、もう少しまとまったものとWordpress初心者の方への説明も加えて、バージョンアップ記事を書いておきます。

導入したいけど手の付け方が分からない、という方の参考になれば幸いです。

逆にすでに導入している、あるいはwordpressについての知識はばっちりという方は、GTFしてください。
※GTF・・・Go to next feed(or Blog).

<h3>基本となるコード</h3>
基本となるコードは以下のリンクからゲットできます。

<a href="http://www.evernote.com/about/intl/jp/developer/sitememory/#a_builder">サイトメモリーボタン</a>

わかりやすいように入力できる部分にすべて文字列を入れてコードをはき出すと以下のようなコードが生成されます。
<blockquote>
&lt;script type="text/javascript" src="http://static.evernote.com/noteit.js"&gt;&lt;/script&gt;
&lt;a href="#" onclick="Evernote.doClip({providerName:'入力項目A',contentId:'入力項目B',suggestNotebook:'入力項目C',code:'入力項目D',title:'入力項目E',url:'入力項目F',suggestTags:'入力項目G'}); return false;"&gt;&lt;img src="http://static.evernote.com/article-clipper.png" alt="Clip to Evernote" /&gt;&lt;/a&gt;
</blockquote>


この入力項目＋アルファベットの部分を入れ替えることでカスタマイズすることができます。

<h3>基本の４つ</h3>
まずは、基本で表示されている４つの入力項目から。

<ul>
	<li>Webサイト名 </li>

	<li>候補となる保存先のノートブック</li>
 
	<li>クリップするコンテンツ</li>

	<li>Evernote紹介コード</li>
  </ul>




<h4>Webサイト名：入力項目A</h4>
空白にしておくと、ドメイン名になります。Blogの名前などを入力しておけばよいでしょう。Wordpressをお使いの方であれば、

&lt;?php bloginfo('name'); ?&gt;

の中にブログのタイトルが入っているのでこれを使うのも一手です。

つまり、

providerName:'&lt;?php bloginfo('name'); ?&gt;'

こんな感じですね。この方法をとっておけば、後でブログのタイトルを変更したときに勝手にクリップの方のタイトルも変更されます。

<h4>候補となる保存先のノートブック ：入力項目B</h4>
当たり障りない対応をしたければ、空白にしておけばよいでしょう。できればタグと同じで提案型であればよかったのですが、今のところEvernoteでのノートブックの使い方の多様性を考えるとけっこう「余計なお節介」な気分がしています。特に「自分のブログのタイトル」を入れるとそうとう「目に付き」ます。

仮に入力するとしても、「自分はこのジャンルで書いているんだ！」ということが明確になっている場合の「ジャンル」を入力しておくぐらいが無難だと思います。

<h4>クリップするコンテンツ：入力項目C</h4>
簡単に説明だけすると「指定したHTMLのID要素に囲まれている部分をクリップ対象にする」というもの。

難しいことを考えたくなければ、テンプレートを見て、一番上最初にでてくる&lt;div id="○○"&gt;を探して、その○○を指定しておけばとりあえずクリップをしてもらうことだけはできます。mainあるいはcontentなどの可能性が高いです。単一記事のテンプレならばこれでも問題ないでしょう。

インデックスページ（トップページ）の場合、これをやってしまうとページ全体がクリップされてしまう可能性があるのでその辺に注意が必要です。

できれば「post」あるいは「entry」という文字列がでてくる付近のidを探した方がよいでしょう。

例えば、テンプレ内に

id="post-&lt;?php the_ID(); ?&gt;"

こういう表記ががあれば、これを指定してしまうのも一手です。つまり

contentId:'post-&lt;?php the_ID(); ?&gt;'

こういう感じに。

もしテンプレの意味がはっきり分かっている方ならば、既存のDivにidを追加するか、クリップ用のDivを追加するか、という選択もできると思います。一応注意すべき点は、id名はそのページ内に一つしか存在してはいけない、というルールになっているということです。class指定の重複は可能ですがid指定は重複不可＿＿言葉の意味から考えても当然ですが＿＿です。これは頭の片隅にでも置いておいてください。

なので、インデックスページでの運用を考えると、独自のIDを作る場合は、

id="clip-&lt;?php the_ID(); ?&gt;"

というようなエントリーごとに異なる名前が割り振られるIDの指定をしておくのが無難でしょう。

<h4>Evernote紹介コード ：入力項目D</h4>
これは好みの問題ですが、アフィリエイト用のコードを埋め込む所です。
アフィリエイトが気になる方＆少々の英語を読むのを厭わない方は、

<a href="http://www.evernote.com/about/affiliate/">http://www.evernote.com/about/affiliate/</a>

からコードを入手して、

code:'rashita△'

みたいな感じでもらったコードを入力してください。

<h3>個別の詳細４つ</h3>
では引き続いて、詳細の方の入力項目も見ていきましょう。

<ul>
	<li>候補となるノートタイトル</li>

	<li>URL</li>

	<li>候補となるタグ</li>
  
	<li>保存様式</li>
</ul>



<h4>候補となるノートタイトル：入力項目E</h4>
空白の場合はページのタイトルが使われますので、単一記事のテンプレの場合は空白でも問題ありません。インデックスページで空白にするとノートのタイトルがブログのタイトルになってしまうので使う人にとっては不便です。

WordPressであれば、

&lt;?php the_title(); ?&gt;

を使うことで、記事のタイトルを持ってくることができます。例えば

title:'&lt;?php the_title(); ?&gt;'
title:'R-style &lt;?php the_title(); ?&gt;'

のような感じが考えられます。

<h4>URL：入力項目F</h4>
これもタイトルと同じ考えで。単一記事の場合は空白でも問題ありません。インデックスページなどは、その記事のURLを引っ張ってくる必要があるので、

&lt;?php the_permalink(); ?&gt;

を使います。こんな感じに。

url:'&lt;?php the_permalink(); ?&gt;'

<h4>候補となるタグ：入力項目G</h4>
これも空白で問題ありませんが、ブログのタイトルやあるいはジャンルなどを入れておけば使う人にとって便利かも知れません。考えられるものとしては
<ul>
	<li>「ブログのタイトル」</li>

	<li>「Blog」「ブログ」</li>
	<li>
「日記」「ニュース」「ネタ」「ハック」などのブログのジャンル</li>
</ul>


があるでしょうか。

以前の記事でも紹介しましたが、ワードプレスの記事のタグをEvernoteのタグとして提案することもできます。具体的には以下のような書式。

suggestTags:'&lt;?php
$posttags = get_the_tags();
if ($posttags) {
foreach($posttags as $tag) {
echo $tag->name . ' ,';
}
}
?>'});

好みに応じてお使いください。
<h4>保存様式</h4>
これは入力項目ではありません。スタイルの保存と言ったところでしょうか。基本的に推奨されている「テキストのみ」を選択しておけば問題ないでしょう。

以下は、「<a href="http://www.evernote.com/about/developer/sitememory/developer.php">開発者向けガイド（英語）</a>」より　
<blockquote>
The clip styling strategy that the clipper should use. Valid values are "none" to ignore page styles, "text" to only apply page styles to textual elements, and "full" to attempt to copy the full styling of the page. The default value is "text", which we suggest using as it yields clips that display consistently across platforms. "full" styling often looks good one one platform but fails to render well on others. Note that there is currently no way to style clips made from IE. 
</blockquote>

超概略意訳：
「none(無し)」はページのスタイルを無視します。「text（テキストのみ）」は文章要素を最適な形で保存します。「full（全て）」はページをまるっとコピーします。デフォはテキストでOK。フルは良いときもあるけども、プラットフォームが変わると酷いときもあるっす。IEくんには要注意だね！

とりあえず、「テキストのみ」を選択しておきましょう。ブログならこれで問題ないはずです。
※テキストのみはデフォルトなのでコードに記入するところはありません。

<h3>どこにつける？</h3>
さて、コードが出来たところでテンプレに追加しましょう。単一記事の表示テンプレと、トップページのテンプレ、この二つを押さえておけば無難です。

記事中のボタン設置の場所ですが、考えられる場所は、記事の前の方か後ろの方だと思います。

今回は記事タイトルの後ろに付けるとして話を進めていきます。テンプレを開いてみて、the_titleとかタイトルがらみの場所を見つけましょう。どこかにあるはずです。大体&lt;h2&gt;あたりで囲まれていると思いますが、テーマごとに違うので断言はできません。もし見つからなければ、一度自分のブログをブラウザで開いてみて、ソースを確認してみてください。右クリックなり、メニューの「表示」なりにあるはずです。

ソースを見たら、記事のタイトルが表示されている部分を探して、そのあたりに出てくる要素を憶えておきます。H2とかあるはclass=""とかが手がかりになるはずです。

あとは、テンプレにかえって先ほどの表示を作っていた部分を探します。発見したらタイトルの直後に、作ったコードを入れればOKです。
※&lt;h2glt;&lt;/h2&gt;でタイトルが表示されていたら、&lt;/h2&gt;の直後に入れる。

ボタンを別の部分に入れる場合でも、おなじような感じで設置場所を見つけてみてください。

コードを入れたら、忘れずに保存（orアップロード）を実行しておきましょう。

<h3>おわりに</h3>
これで大体WordpressでのSiteMemoryボタンの導入はできるのではないかと思います。ページのテーマにもよりますが、完璧に対応するのであれば、

<ul>
	<li>tag.php (tag.php)</li>

	<li>アーカイブ (archive.php)</li>

	<li>カテゴリーテンプレート (category.php)</li>

	<li>ページテンプレート (page.php)</li>

	<li>メインインデックスのテンプレート (index.php)</li>

	<li>単一記事の投稿 (single.php)</li>

	<li>検索結果 (search.php)</li>
</ul>



あたりのテンプレをいじる必要があります。

あと、おまけ的な紹介になりますが、すでにプラグインがあります。

<a href="http://blog.makotokw.com/2010/09/13/evernote-site-memory-for-wordpress%E3%83%97%E3%83%A9%E3%82%B0%E3%82%A4%E3%83%B3/">Evernote Site Memory for WordPressプラグイン</a>（kwLog）

<a href="http://blog.makotokw.com/portfolio/wordpress/site-memory-for-wordpress/">使い方</a>(kwLog)

最新のバージョンがどうなっているのかはわかりませんが、自分でボタンを導入したい場所にコードを埋め込む作業は必要な感じです。

プラグインのサイトはこちら

<a href="http://wordpress.org/extend/plugins/site-memory-for-wordpress/">http://wordpress.org/extend/plugins/site-memory-for-wordpress/</a>

自分で一からやるも良し、テンプレの助けを借りるも良しです。Evernoteを使っていてるブロガーの方は、「おれもEvernote使っているよ」のアピールと共にボタンを設置してみてはいかがでしょうか。

▼こんな一冊も：
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540728%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540728" target="_top">EVERNOTE「超」仕事術</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540728%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540728" target="_top"><img src="http://ecx.images-amazon.com/images/I/51zkZf06QlL._SL160_.jpg" border="0" alt="EVERNOTE「超」仕事術" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />シーアンドアール研究所  2010-08-18<br />売り上げランキング : 478<br /><br /><strong>おすすめ平均  </strong><img src="http://g-images.amazon.com/images/G/01/detail/stars-4-0.gif" alt="star" /><br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-3-0.gif" alt="star" />クラウド時代のGTD指南本<br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-4-0.gif" alt="star" />GTDに使えそうです<br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-5-0.gif" alt="star" />EVERNOTEを利用した『知的生産の技術』指南本<br /><br /><a href="http://www.amazon.co.jp/EVERNOTE%E3%80%8C%E8%B6%85%E3%80%8D%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2/dp/4863540728%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863540728" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

