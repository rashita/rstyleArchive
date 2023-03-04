---
title : CSSの知識が無いまま、Wordpressを始めて右往左往している人への「デザインの一歩目」
link : 4035
date : Wed, 16 Jun 2010 00:11:33 +0000
categories : ["4-僕らの生存戦略"]
tags : ["wordpress","セルフ・ブランディング"]
draft : false
author : 倉下忠憲
---

なにやら今更感タップリな話ですが、「セルフブランディング」を意識してブログを始めた、という方がおられるかも知れないのでちょっと書いておきます。基本的な知識をお持ちの方には何の意味もないエントリーなので、「Go to next feed」しちゃってください。

また、本格的にごりごり作り込みたいレベルに達することもできません。細かい知識は専門的なサイトでフォローしてみてください。今回の記事は「最低限のデザイン変更はどうやったらできるのか」という内容です。

<h3>編集はどこで？</h3>
基本的には、Wordpress(以下WP)の管理者ページから変更することが可能です。日本語であれば、

「サイドバー」→「外観」→「編集」

で、デザインの編集を行うことができます。

<h3>テーマを選ぼう</h3>
「いちから細かく作り込もう」と勢い立つのは良いのですが、かなり面倒なのであまりオススメしません。

もともと提供されているテーマが数多くありますので、その中から自分好みのものを探すのが一番楽です。またオリジナルなテーマを提供しているウェブサイトもありますので、その辺をうろちょろしてみてもよいでしょう。

テーマを探すには、

「サイドバー」→「外観」→「新しいテーマの追加」

からさまざまな条件で検索することができます。条件のすべてが理解できなくても、以下のポイントだけは押さえておいたほうが良いと思います。

・「色」
・「列」
・「幅」

この３つは、あとで「ちょっとだけ変える」ということが難しいので、この３つの要素を軸にして好みのテーマを探しましょう。

普通のブログスタイルならば、3列か左右どちらかのサイドバーが良いかなと思います。

ブログパーツやガジェット類を大量に追加予定ならば3列タイプを、そんなに「マッチョ」には詰め込まないというならば、2列、右サイドバー、左サイドバー、あたりで十分でしょう。

<h3>テーマの中身ファイル</h3>
もしかしたら、選択したテーマでデザインは十分満足、という方もおられるかも知れません。そういう方はここで終了です。思う存分ブログライフをお楽しみ下さい。ただ、ちょっとフォントのサイズが・・・とか記事タイトルの色を変えたい、という方は手を加える必要があります。

先ほど提示した

「サイドバー」→「外観」→「編集」

の画面を確認しましょう。

テーマファイルの中に「テンプレート」と「スタイル」の二つの項目があると思います。大体テンプレートファイルが２０程度、スタイルは１つという所でしょうか。

何か一つファイルを選択すれば、テキストエリアにその内容が表示されるはずです。もしこのときに下の方に「ファイルを更新」ボタンが表示されていないか、「更新はできません」という類の文句がでている場合、サーバー上のファイルが変更できない設定になっています。

FTPソフトなどで「ファイル属性の変更」を行って下さい。
※<a href="http://siriasu.s10.xrea.com/ffftp/ffftp.htm">FFFTPの使い方</a>などを参照のこと。
<h3>phpって何？</h3>
テンプレートファイルは拡張子phpが、スタイルファイルには拡張しcssが付いていると思います。これがいったい何なのかを理解する必要は特にありません。大体以下のようなアバウト理解で十分です。

・php →構造設計図
・css →デザイン設計図

phpで要素の配置などを指定し、色やフォントなどはcssで指定する、ということです。これも詳しい話を書き出すときりがありません。

phpは構造設計図なので、ウェブブラウザで閲覧するときはそのファイルの内容が直接表示されるわけではありません。書かれている内容に基づいて、「あれをここに配置」「あそこからこれをロードして表示」「別のテンプレートを呼び出して表示」という感じでページを作っていきます。

つまり、ページの骨組みを変えたければこのphpファイルを変更すればよいということですが、これはやや敷居が高いものでもありますし今回のテーマからは外れるので割愛します。そういう部分はしっかりとテーマを選んで回避してください。
※もちろん最終的にいろいろいじり回したければある程度の理解は必要

配置された要素を「どんな感じで表示するのか」という指定が書かれたものがcssファイルです。今回はこちらを修正することで文字サイズなどを変更するお話です。

<h3>スタイルシートの中身</h3>
ちなみに、まったくどうでも良い話ですが、CSSは「カスケーディング・スタイル・シート」の略語です。カスケーディングって何やねん、という疑問に答えるにはCSSの全体像に迫る必要があるのでするっと割愛しておきます。とりあずcssはスタイルシートなんだな、というぐらいで把握しておいて下さい。

さて、スタイルシートの変更です。おそらく「Stylesheet (style.css)」というファイルがあると思うので、それをクリックしてテキストエリアに表示させましょう。

cssファイルをざらって見てもらうと分かりますが、大まかに以下のような感じのものがずらずら並んでいると思います。


<blockquote>
要素名　{
スタイル名:スタイル指定;
}</blockquote>



要素名も#付きのもの、アルファベット（＋数字）だけ、”.”が頭に付いてアルファベットが並んでいるもの、とさまざまあるはずです。

<h3>治療場所の発見</h3>
まず最初にすべきは、自分のブログを表示することです。トップページを開いたら、その「ソース」を確認してみましょう。Firefoxなら「表示」の「ページのソース」から確認できます。
※右クリック「ページのソースを表示」でも同様

ソースをずらずらと眺めていくと、先ほど#付きで提示されていたような要素名が並んでいるのに気がつくでしょう。#が付いていると何が起こるのか、という事は一端置いておいて、これらが対応しているということを理解しておいて下さい。
※ちなみに、"#"付きが「id」で"."付きが「class」に対応しています。

とりあえず、ソースを確認して自分が今変えたいと思っているのがどこの部分なのかを確認してみましょう。

もしブログのタイトル部分のフォントサイズがちょっと小さいなと思ったら、その部分を探します。仮に、以下のような部分を発見したとします。



<blockquote>＜div id="header"＞

		＜h3＞＜a href="https://rashita.net/blog/"＞R-style＜/a＞＜/h3＞</blockquote>



これが、タイトルを表示している部分です。治療する場所は見つかりました。

<h3>スタイルシートの変更</h3>
同様に、先ほどのスタイルシートの編集画面から類似する場所を探します。すると「#header」という部分が見つかるはずです。でも、そこではありません。もう少し探してみましょう。すると「#header h3」という項目が見つかるでしょう。そこが対応箇所です。

この「#header h3」というのは、#deader(つまりid="header")内部にある、h3のスタイルを変えちゃいますよ、という意味合いです。発見した箇所にはもともとある程度スタイルが指定されているはずです。例えばこんな感じに。


<blockquote>
#header h3{
margin:  0;
padding: 15px 0 0 15px;
font-weight:800;
font-size: 200%;
}
</blockquote>


フォントサイズを変えたければ、「font-size: 200%;」の200%の部分を自分の好みの数に変更すればそれでOKです。変更したら「ファイルを更新」ボタンをぽちっと押しておけばOKです。

※もし、どうしてもこれが見つからないというのであれば、一番下の方に自分で書き加えましょう。
<h3>よくあるスタイル</h3>
先ほどはフォントのサイズを変更しました。フォントのサイズ変更は

<em>font-size: 200%;</em>

というような指定をします。200%の部分はパーセンテージ以外にもさまざまな指定の方式がありますが、その辺は詳しいサイトさんを見て下さい。これ以外によく使われるのが

<em>font-family: sans-serif;
color:black ;
text-decoration: none;
</em>
というものです。

「font-family」はフォント名を指定します。「color」はテキストの色を指定。色名以外にも「#FFFFFF」のようなRGB指定もできます。「text-decoration」は文字の飾り付けを指定します。「none」(なし)を指定すれば、リンクのアンダーラインを消すことができます。

<h3>まとめ</h3>
これ以外にもさまざなCSSがあって、それらを使いこなせば、Coolなブログを作ることができますが、とりあえずはカッコイイテーマを探して、あとはテキストの色なりサイズを変えることから始めてみましょう。

ここで紹介したものは単なる入り口です。本格的にカスタマイズしたければ、自分でソースを見て、CSSの要素名を覚え、Wordpressの構造を知る必要があります。ただ、そこまで強くこだわる必要はないのではないかと、個人的には考えています。どうしても既存のテーマに物足りなさを感じたときに、ちょっと調べてみる程度のお付き合いでよいのではないでしょうか。

<strong>▼要素名をとりあえず知りたい方は</strong>
<a href="http://www.tohoho-web.com/www.htm">とほほのWWW入門</a>

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/%E3%83%91%E3%83%BC%E3%82%BD%E3%83%8A%E3%83%AB%E3%83%BB%E3%83%9E%E3%83%BC%E3%82%B1%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0-%E6%9C%AC%E7%94%B0-%E7%9B%B4%E4%B9%8B/dp/488759755X%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D488759755X" target="_top">パーソナル・マーケティング</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/%E3%83%91%E3%83%BC%E3%82%BD%E3%83%8A%E3%83%AB%E3%83%BB%E3%83%9E%E3%83%BC%E3%82%B1%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0-%E6%9C%AC%E7%94%B0-%E7%9B%B4%E4%B9%8B/dp/488759755X%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D488759755X" target="_top"><img src="http://ecx.images-amazon.com/images/I/41KJ3ZWiiVL._SL160_.jpg" border="0" alt="パーソナル・マーケティング" /></a></td><td valign="top"><font size="-1">本田 直之 <br /><br />ディスカヴァー・トゥエンティワン  2009-11-19<br />売り上げランキング : 4102<br /><br /><strong>おすすめ平均  </strong><img src="http://g-images.amazon.com/images/G/01/detail/stars-4-0.gif" alt="star" /><br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-4-0.gif" alt="star" />すでにセルフブランディングの「コア」となるものをもつ人にとってはきわめて有用な本<br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-4-0.gif" alt="star" />パーソナルマーケティングで人生が輝く!<br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-5-0.gif" alt="star" />ワークの実践が重要です。<br /><br /><a href="http://www.amazon.co.jp/%E3%83%91%E3%83%BC%E3%82%BD%E3%83%8A%E3%83%AB%E3%83%BB%E3%83%9E%E3%83%BC%E3%82%B1%E3%83%86%E3%82%A3%E3%83%B3%E3%82%B0-%E6%9C%AC%E7%94%B0-%E7%9B%B4%E4%B9%8B/dp/488759755X%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D488759755X" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/WordPress%E3%83%AC%E3%83%83%E3%82%B9%E3%83%B3%E3%83%96%E3%83%83%E3%82%AF-2-8%E5%AF%BE%E5%BF%9C%E2%80%95%E3%82%B9%E3%83%86%E3%83%83%E3%83%97%E3%83%90%E3%82%A4%E3%82%B9%E3%83%86%E3%83%83%E3%83%97%E5%BD%A2%E5%BC%8F%E3%81%A7%E3%83%9E%E3%82%B9%E3%82%BF%E3%83%BC%E3%81%A7%E3%81%8D%E3%82%8B-%E3%82%A8%E3%83%93%E3%82%B9%E3%82%B3%E3%83%A0/dp/4883376737%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4883376737" target="_top">WordPressレッスンブック 2.8対応―ステップバイステップ形式でマスターできる</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/WordPress%E3%83%AC%E3%83%83%E3%82%B9%E3%83%B3%E3%83%96%E3%83%83%E3%82%AF-2-8%E5%AF%BE%E5%BF%9C%E2%80%95%E3%82%B9%E3%83%86%E3%83%83%E3%83%97%E3%83%90%E3%82%A4%E3%82%B9%E3%83%86%E3%83%83%E3%83%97%E5%BD%A2%E5%BC%8F%E3%81%A7%E3%83%9E%E3%82%B9%E3%82%BF%E3%83%BC%E3%81%A7%E3%81%8D%E3%82%8B-%E3%82%A8%E3%83%93%E3%82%B9%E3%82%B3%E3%83%A0/dp/4883376737%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4883376737" target="_top"><img src="http://ecx.images-amazon.com/images/I/51ax8oRVxrL._SL160_.jpg" border="0" alt="WordPressレッスンブック 2.8対応―ステップバイステップ形式でマスターできる" /></a></td><td valign="top"><font size="-1">エビスコム <br /><br />ソシム  2009-09<br />売り上げランキング : 2319<br /><br /><strong>おすすめ平均  </strong><img src="http://g-images.amazon.com/images/G/01/detail/stars-4-5.gif" alt="star" /><br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-5-0.gif" alt="star" />基礎から勉強したい人には是非おすすめ<br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-5-0.gif" alt="star" />理解しやすいです。<br /><img src="http://g-images.amazon.com/images/G/01/detail/stars-5-0.gif" alt="star" />カスタマイズを理解したいなら最初にこれを買うべき<br /><br /><a href="http://www.amazon.co.jp/WordPress%E3%83%AC%E3%83%83%E3%82%B9%E3%83%B3%E3%83%96%E3%83%83%E3%82%AF-2-8%E5%AF%BE%E5%BF%9C%E2%80%95%E3%82%B9%E3%83%86%E3%83%83%E3%83%97%E3%83%90%E3%82%A4%E3%82%B9%E3%83%86%E3%83%83%E3%83%97%E5%BD%A2%E5%BC%8F%E3%81%A7%E3%83%9E%E3%82%B9%E3%82%BF%E3%83%BC%E3%81%A7%E3%81%8D%E3%82%8B-%E3%82%A8%E3%83%93%E3%82%B9%E3%82%B3%E3%83%A0/dp/4883376737%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4883376737" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

<div class="column">
<strong>編集後記：</strong>
今回は、ちょっとだけデザインを変える人向けに、かなり限定的に書きました。理解が不十分にしか進まない箇所だらけですが、応急処置はできるのではないかと思います。もし、本楽的に知りたい人がおられるならば、また詳しい解説を書いてみます。
</div>


