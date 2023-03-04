---
title : 『ブログを10年続けて、僕が考えたこと』のScrivenerのファイル構成およびcompileの設定と使用したCSSファイルについて
link : 16140
date : Wed, 03 Jun 2015 03:08:48 +0000
categories : ["scrivenerへの散歩道","物書き生活と道具箱"]
tags : ["scrivener","でんでんコンバーター","セルフパブリッシング","電子書籍"]
draft : false
author : 倉下忠憲
---

先日発売した以下の新刊ですが、

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/%E3%83%96%E3%83%AD%E3%82%B0%E3%82%9210%E5%B9%B4%E7%B6%9A%E3%81%91%E3%81%A6%E3%80%81%E5%83%95%E3%81%8C%E8%80%83%E3%81%88%E3%81%9F%E3%81%93%E3%81%A8-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00YI05M1K%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00YI05M1K" target="_blank">ブログを10年続けて、僕が考えたこと</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/%E3%83%96%E3%83%AD%E3%82%B0%E3%82%9210%E5%B9%B4%E7%B6%9A%E3%81%91%E3%81%A6%E3%80%81%E5%83%95%E3%81%8C%E8%80%83%E3%81%88%E3%81%9F%E3%81%93%E3%81%A8-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00YI05M1K%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00YI05M1K" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41qzGeKnNEL._SL160_.jpg" border="0" alt="ブログを10年続けて、僕が考えたこと" /></a></td><td valign="top"><font size="-1">倉下忠憲 <br /><br />倉下忠憲  2015-05-28<br />売り上げランキング : 1809<br /><br /><br /><a href="http://www.amazon.co.jp/%E3%83%96%E3%83%AD%E3%82%B0%E3%82%9210%E5%B9%B4%E7%B6%9A%E3%81%91%E3%81%A6%E3%80%81%E5%83%95%E3%81%8C%E8%80%83%E3%81%88%E3%81%9F%E3%81%93%E3%81%A8-%E5%80%89%E4%B8%8B%E5%BF%A0%E6%86%B2-ebook/dp/B00YI05M1K%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00YI05M1K" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

あいかわらず作成に使ったツールは同じです。

Scrivenerでテキストを構成し、.txtに出力。それを<a href="http://conv.denshochan.com/" target="_blank">でんでんコンバーター</a>変換して、KDPにアップロードという流れ。

でんでんコンバーターで少し凝ったデザイン（組版的な意味で）を行う場合は、作成後のepubファイルをzipにして開くことが必要だったりするわけですが、今回の本はでんでんコンバーターからの出力一発となっております。

それはあらかじめ「仕込んである」からなんですが、その辺も含めて今回は中身の方を紹介してみましょう。

<span class="appIcon"><img class="appIconImg" height="60" src="http://is3.mzstatic.com/image/pf/us/r30/Purple1/v4/f0/17/37/f0173777-a6a4-3bdc-78a7-aaa3aa83fb5b/Scrivener.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store">Scrivener</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, 教育</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

<H3>ファイル・フォルダ構成</H3>

まずはScrivenerの中身から。

ファイル＆フォルダ構成はこのようになっています。

<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot1.png" alt="screenshot" width="240" height="521" class="alignnone size-full wp-image-16141" /></a>

まず「原稿」という大きなフォルダがあり、その下に本の素材となるファイルとフォルダが並んでいます。フォルダは章ごとに１つあり、その下にそれぞれの章の本文となるファイルが並んでいます。ただし、「扉」というファイルは「原稿」フォルダの直下に置いてある点に注意してください。後ほどのcompileでこの配置が効いてきます。

続いて、本文の中身。

<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot2-1024x401.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-16142" /></a>

上の画像は、第一章のフォルダの中身です。第一章のテキストを収めたファイルがここにすべて含まれているわけですが、冒頭の数行に関しては、フォルダの中にあるファイルではなく、フォルダに直接書き込んである内容です。いちおう書いておきますと、Scrivenerのフォルダは、直下にファイルやフォルダを配置するだけのものではなく、そこに直接テキストを書き込むこともできます。
※テキストを入力すると、アイコンの表示が変わります。

こちらは「扉」のテキスト。

<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot3-1024x443.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-16143" /></a>

ご覧の通り、マークダウンではなくがっつりHTMLが使われています。ここが組版的デザインのポイントで、でんでんマークダウンだけだとclassの指定ができないので、「じゃあ、もう直接HTML入れとくか」のノリで、それが記入されています。もちろん、対応するCSSもCSSファイル内に書き込んであるわけですが、それはまた後ほど。

<H3>separateの設定</H3>

separateの設定は次のようになっています。

<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot4.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot4.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-16144" /></a>

ほかはすべてシングルリターンですが、ファイル→フォルダの境界だけカスタム設定として「===」が入ります。「===」は、でんでんマークダウンで「（ファイル分割によって）改ページせよ」として機能します。先ほどのファイル構成をもう一度ご覧ください。

<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot1.png" alt="screenshot" width="240" height="521" class="alignnone size-full wp-image-16141" /></a>

ファイル→フォルダの境界となるのは（ファイルの次にフォルダが出てくるのは）、

「扉ファイル」→「第一章のフォルダ」
「第一章のラストファイル」→「第二章のフォルダ」
「第二章のラストファイル」→「第三章のフォルダ」
「第三章のラストファイル」→「第四章のフォルダ」
「第四章のラストファイル」→「第五章のフォルダ」
「第五章のラストファイル」→「おわりにのフォルダ」

の６つです。これはつまり、章と章の境目です。ここに改ページが入るようになっています。

このseparateの設定を使わず、本文に直接「===」を記入していっても、できあがるepubは同じです。ただし、こうした設定をしておくと、「記入し忘れる」というミスを防ぐことができます。また、校正作業でファイルの順番を入れ換えても、いちいち「===」の場所を移動させる必要がありません。

<H3>formattingの設定</H3>

formattingは、３つのパターンを使用しています。「第二階層のフォルダ」「第二階層のファイル」「第三階層のファイル」の３つです。
※第一階層のフォルダは、「原稿」という一番上のフォルダなので使用しません。またその階層にはファイルはありません。

一番簡単なのは、「第三階層のファイル」です。

<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot8.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-16148" /></a>


ここには本文が入っています。そこで、titleとtextを選択し、titleの接頭辞として、「### 」を指定します。

ここでのtitleはファイルやフォルダの名前ですので、たとえば「ブログの流れは絶えずして」というファイルならば、

<blockquote>
### ブログの流れは絶えずして

ここから本文
</blockquote>

といった感じでcompileされるわけです。
※###はでんでんコンバーターにおけるH3の指定。


<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot5.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot5.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-16145" /></a>


続いて「第二階層のファイル」。

ここに位置するのは、「扉」というファイルだけです。で、名前の通りこのページは扉ページなのですが、一行だけの言葉が置いてあります。このページを「第三階層のファイル」と同じにしてしまうと、少し問題が発生します。

<blockquote>
### 扉

あなたのブログが、良き読者と共にあらんことを。
</blockquote>

このように、でかでかと(h3で）「扉」と表示されることになるのです。さすがにそれはダサいです（あと、表示上の問題もあるのですが、それは後ほど）。

そこで、第二階層のファイルは、textは選択するものの、titleは選択していません。

というか話はまったく逆で、このファイルだけtitleを選択したくないので階層を分けているのです。

<H3>章の扉ページ</H3>

<a href="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/06/screenshot7.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-16147" /></a>

一番ややこしいのが「第二階層のフォルダ」です。章のトップページに位置する要素です。

ここで使用するのはtitleとtext。そこまでは普通なのですが、接頭辞と接尾辞が込み入っています。

接頭辞と接尾辞は、簡単に言えば、

[○○ title △△]

の○○（接頭辞）と△△（接尾辞）を指定するものです。「第三階層のファイル」ではこの接頭辞を使用しました。で、この○○と△△にはなんでも入力できます。たとえば、○○に&lt;h2&gt;を、△△に&lt;/h2&gt;を指定すれば、compile時には、

&lt;h2&gt;title&lt;/h2&gt;

となるわけです。そして、接頭語・接尾語には複数行を入力することも可能です。ということは、

<blockquote>
&lt;section class="titlepage"&gt;

&lt;div class="titlepage-container"&gt;

&lt;div class="titlepage-collectiontitle-placeholder"&gt;&lt;/div&gt;
                &lt;h2 class="titlepage-maintitle"&gt;
</blockquote>

を接頭辞に、

<blockquote>
&lt;/h2&gt;
&lt;div class="titlepage-subtitle-placeholder"&gt;&lt;/div&gt;
 &lt;hr style="border-top: 2px solid #bbb;" /&gt;
&lt;p class="titlepage-creator"&gt;&lt;/p&gt;
&lt;/div&gt;
&lt;/section&gt;
</blockquote>

を接尾辞に指定することも可能ということです。

そしてこれは、でんでんコンバーターが自動的に作成してくれる扉ページHTML（titlepage.xhtml）のほぼそのままのパクリでもあります（ある程度はカスタマイズしてあります）。

<H3>スタイルシート</H3>

が、単にこうしたコードを埋め込んでも、CSSが指定されていなければデザイン上の意味はありません。でんでんコンバーターが作成するtitlepage.xhtmlは、template.cssという特別のスタイルシートが当たっており、本文中に適用されるstyle.cssとは隔離されているのです。

だったら、混ぜてしまいましょう。

<script src="https://gist.github.com/rashita/4e7860a7ecdde88efb24.js"></script>

でんでんコンバーターの標準のスタイルシートに、epubをzip解体して中身を覗いたtemplate.cssを上乗せしてあります。これで、titlepage.xhtmlで使われているclass指定がそのまま使えます。

その他、標準のスタイルシートから変更を加えている点は、

<ul>
<li>blockquote,ulのフォントサイズをやや小さく</li>
<li>h3のmargin-bottomを少し広く</li>
<li>エピグラフ用のCSSを追加（フォント小さく、右寄せ）</li>
<li>h3のpage-break-beforeを常に</li>
</ul>

あたりです。

最後の「h3のpage-break-before」はページ制御で、h3の手前で改ページが入るようになっています。見出しごとにページの区切りがあるわけです。

しかし、この指定では、本の一番最初のページがh3で始まっていると、特に意味のない空白ページが生まれてしまいます。本の一番最初の要素がh3→その手間に改ページを入れなければならない→しかし、その手間には何の要素もない→空白のページが誕生、こういう流れです。

そこで、扉ページだけ第一階層に切り分けてtitleを入れないようにしているわけです。こうしておけばh3が入ることはありません。つまり、ここだけ手間に改ページを入れることを避けられるわけです。

この切り分けの強力さは、たぶん実際にcompileを体験してみないと理解しにくいかと思いますが、相当に便利な手法であることをここに宣言しておきます。

<H3>さいごに</H3>

以上のような、一見ややこしく、その実やっぱりややこしいことをいろいろやっております。

ただ、仕組みを理解するとすごく楽であることは間違いありません。構成を整えていると、文章の順番は結構な頻度で変わります。そのたびごとに、ページ構造を意識してコードを書き換えるのはわりと面倒なのです。

というわけで、上記の設定を確認しながら、実際に本の中身もチェックしてみるとより一層理解が進むかもしれません。宣伝です。