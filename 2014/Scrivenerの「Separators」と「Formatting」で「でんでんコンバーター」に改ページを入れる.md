---
title : Scrivenerの「Separators」と「Formatting」で「でんでんコンバーター」に改ページを入れる
link : 14273
date : Mon, 08 Sep 2014 02:31:16 +0000
categories : ["scrivenerへの散歩道"]
tags : ["epub","scrivener","でんでんコンバーター"]
draft : false
author : 倉下忠憲
---

先週のエントリーで、Scrivenerにおける改ページを紹介しました。

<a href="https://rashita.net/blog/?p=14255" target="_blank">Scrivenerへの散歩道#011　ページを制御する</a>

が、最終的な着地点をEPUB３と想定する場合、Scrivenerさんはやや非力です。コンパイルとして書き出せるEPUBのフォーマットがEPUB2なのです。

というわけで、Scrivenerからプレーンテキストで書き出し、それをわれらが「<a href="http://conv.denshochan.com/" target="_blank">でんでんコンバーター</a>」で変換する、というのが最近の私のお気に入りの手順なわけですが（※）、その場合、改ページの手法が変わってきます。
※詳しくは<a href="https://rashita.net/blog/?p=13496" target="_blank">こちらのエントリーを</a>。

今回は、その手法について紹介しましょう。

<span class="appIcon"><img class="appIconImg" height="60" src="http://a4.mzstatic.com/us/r30/Purple4/v4/59/f5/79/59f57985-7c59-0b0c-48ba-cf8fc7bfd9e5/Scrivener.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store">Scrivener</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, 教育</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

<H3>でんでんコンバーターにおける改ページ</H3>

基本的なところから確認します。

「でんでんコンバーター」における改ページは、ファイル分割によって行われます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot11.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14275" /></a>

シンプルに言えば、イコール記号「=」を３つ以上入れれば、そこで改ページが行われるよ、ということです。まずは、それを覚えておいてください。

実際は、その部分でファイル分割が行われます。通常であれば、EPUBファイルを構成するxhtmlファイルは、

bodymatter_0_0.xhtml

の一つなのですが、イコール記号「=」を３つ以上入れた行があれば、

bodymatter_0_0.xhtml
bodymatter_0_1.xhtml

となります。一つのファイルが二つに分割されたわけです。

電子書籍リーダーは、これらのファイルを連続で表示しますが、ファイルとファイルの境目に「改ページ」が生まれます。

一般的には、たとえば章ごとに、改ページ（ファイル分割）を入れておくのがスマートでしょう。大きすぎるファイルは、表示も遅くなるそうで、宗教的制約がないかぎりは、改ページ（ファイル分割）を使うのが吉です。

<H3>あたまとおしりに自動的に追加</H3>

Scrivenerを使う場合は、いちいちイコール記号を入れて回る必要はありません。コンパイル時のオプションで指定可能です。

方法は二つ。「Separators」あるいは「Formatting」。どちらも、境目に自動的に文字列を挿入する方法ですが、前者はおしりに、後者はあたまに挿入することになります。

<H4>「Separators」</H4>

まずは、「Separators」から。こちらは、ファイルとファイルの境目の制御です。たとえば、改行を入れるのか、入れないのか、といった制御になります。

オプションでは、以下のように表示されているでしょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot12.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot12.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14276" /></a>

<ul><li>テキストとテキストの間</li>
<li>フォルダとフォルダの間</li>
<li>フォルダとテキストの間</li>
<li>テキストとフォルダの間</li></ul>

この４つの指定箇所があり、それぞれ、

<ul><li>Single return</li>
<li>Empty line</li>
<li>Page break</li>
<li>Custom</li></ul>

の４つが選べます。

ここで「Page break」を選択すれば、前回のページビューにおける改ページが入るのですが、今回注目したいのはCustomで、これを選択すると<strong>任意の文字列</strong>を間に挿入できます。

任意の文字列？

そう、イコール記号三つ以上ですね。

具体例を挙げてみましょう。

まず、「テキストとフォルダの間」に「===」を指定します。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/f006b5a4bef184c9608357376220a8a9.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/f006b5a4bef184c9608357376220a8a9.png" alt="f006b5a4bef184c9608357376220a8a9" width="491" height="303" class="alignnone size-full wp-image-14280" /></a>

ファイルの構成は次のような感じ。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot13.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot13.png" alt="screenshot" width="279" height="83" class="alignnone size-full wp-image-14277" /></a>

コンパイルで出力されるテキストファイルは、こうなります。無事、改ページ記号が自動挿入されました。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot14.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot14.png" alt="screenshot" width="390" height="183" class="alignnone size-full wp-image-14278" /></a>

Scrivenerでは、フォルダを使って章立てを分ける構成がよく行われますが、たとえば、以下のようなファイル構成ならば、

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot15.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot15.png" alt="screenshot" width="173" height="477" class="alignnone size-full wp-image-14279" /></a>

「テキスト→フォルダ」のセパレーターに改ページ記号を指定しておくと、でんでんコンバーターでの変換時に、ばっちり改ページ（ファイル分割）が行われます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/0046af8727f0608b16069cf7c5cdd34f.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/0046af8727f0608b16069cf7c5cdd34f.png" alt="0046af8727f0608b16069cf7c5cdd34f" width="173" height="477" class="alignnone size-full wp-image-14282" /></a>
※注意:フォルダのtitleが出力されないと、セパレーターも挿入されません。

ちなみに、「テキスト→フォルダ」のテキスト部分に直接改ページ記号を書き込んだとしても、コンパイル時のテキストファイルの見た目は同じになります。

しかし、この場合、構成をいじり、テキストの配置が変わってしまった場合、改ページ記号の場所も変更する必要があります。「Separators」で指定しておけば、どれだけ中身が変わっても、「テキスト→フォルダ」の間には改ページ記号が入ることになるので、手間が少ないと言えるでしょう。

<H4>「Formatting」</H4>

もう一つが、「Formatting」ですが、これについては以前ブログで書きました。

<a href="https://rashita.net/blog/?p=13506" target="_blank">二冊目の電子書籍の製作手順（２）　〜Scrivener→「でんでんコンバーター」のちょっとしたコツ〜</a>

上の記事の中頃に出てきます。

こちらはテキストあるいはフォルダの頭の部分に指定した文字列を入れる方法ですが、階層ごとに指定を分けられるので、フォルダの中にフォルダがあって「Separators」ではうまくいかない……、みたいな場合には便利でしょう。

「Separators」と「Formatting」のどちらが正しいということはありません。機能の特徴を踏まえながら、パズルを解くように手間少なく改ページを入れる方法を編み出してください。

<H3>CSSによる強制的な改ページ</H3>

改ページはしたいけど、ファイル分割はちょっと……という場合もありますね。

たとえば私のエッセイ集は30とか50とかのエッセイが入っていて、それぞれ改ページしてあります。もし、すべてをファイル分割すると、30とか50のxhtmlファイルができあがるわけです。まあ、読む人には関係無いのでそれでも良いと言えば良いのですが、ファイル分割を行わない、改ページの方法もあります。

それは、CSSの「page-break」を使う方法です。

<a href="http://www.htmq.com/style/page-break-before.shtml" target="_blank">page-break-before</a>（HTMLクイックリファレンス）
<a href="http://www.htmq.com/style/page-break-after.shtml" target="_blank">page-break-after</a>（HTMLクイックリファレンス）

たとえば、H2がエッセイのタイトルになっているならば、H2タグに"page-break-before:always"を指定しておけば、H2が登場する度に、その前に改ページが入ります。ちなみに、ラフに指定すると、どこに登場するH2にも効果が発生してしまうので、改ページしたくないところで改ページになってしまう可能性がある点には注意。

が、どうやって指定したらいいのか、という話は本稿の手に余りますので、適当にググってみてください。

<H3>さいごに</H3>

ふつうに作っている分には、章と章の間で改ページを入れる方法で問題ないでしょう。

数が少なければ、上記の話は一切無視して手で入力していくのもありです。が、構成が大きければ、Scrivenerのコンパイルオプションは非常に便利ですので、覚えておいてください。

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">KDPではじめる セルフパブリッシング</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank"><img src="http://ecx.images-amazon.com/images/I/51XYQ5BxD0L._SL160_.jpg" border="0" alt="KDPではじめる セルフパブリッシング" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />シーアンドアール研究所  2013-12-21<br />売り上げランキング : 535375<br /><br /><br /><a href="http://www.amazon.co.jp/KDP%E3%81%A7%E3%81%AF%E3%81%98%E3%82%81%E3%82%8B-%E3%82%BB%E3%83%AB%E3%83%95%E3%83%91%E3%83%96%E3%83%AA%E3%83%83%E3%82%B7%E3%83%B3%E3%82%B0-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4863541384%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4863541384" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

