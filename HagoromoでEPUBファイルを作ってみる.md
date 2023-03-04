---
title : HagoromoでEPUBファイルを作ってみる
link : 13372
date : Wed, 21 May 2014 01:26:36 +0000
categories : ["物書き生活と道具箱"]
tags : ["hagoromo","電子書籍"]
draft : false
author : 倉下忠憲
---

先日HagoromoというMacのエディタを紹介しました。

<span class="appIcon"><img class="appIconImg" height="60" src="http://a3.mzstatic.com/us/r30/Purple6/v4/16/69/7d/16697da8-bb23-8206-01df-99dbb9dc5b83/hagoromoApp.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/hagoromo/id865949654?mt=12&uo=4&at=11l4y8" target="itunes_store">Hagoromo</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, ビジネス</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/hagoromo/id865949654?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

<a href="https://rashita.net/blog/?p=13330" target="_blank">Macのエディタ「Hagoromo」に注目しています</a>（r-style）

<blockquote>
私が注目しているポイントは３つ。
	•縦書き・原稿用紙ビューがある
	•アウトライン機能がある
	•EPUB出力できる
</blockquote>

今回は、三番目の「EPUB出力」をピックアップします。

とりあえず、実際にEPUBファイルを作ってみましょうか。

<H3>作る前に確認</H3>

まずは、要素の確認です。

メニューの「ファイル」→「ePubとして書き出す…」を選択しましょう。以下のようなメニューが表示されるかと思います。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot13.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot13.png" alt="screenshot" width="383" height="525" class="alignnone size-full wp-image-13373" /></a>

１）タイトルは、そのままタイトル。デフォルトではファイル名が入るようです。

２）著者も、そのまま著者名。「環境設定」の「新規書類」→「プロパティ」でデフォルトの著者名が設定可能。

３）ジャンルはリストからの選択になっています。選べるのは一つだけ。

※一例
<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot15.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot15.png" alt="screenshot" width="269" height="170" class="alignnone size-full wp-image-13375" /></a>

４）見慣れないのは「識別子」でしょうか。これは「この本は、この本です」ということを確認するためのメタデータで、「ユニーク識別子」とも呼ばれます。詳しくは以下のページをどうぞ。

<a href="http://epubcafe.googlecode.com/svn/trunk/tutorial/OEBPS/Text/Chapter030203.xhtml" target="_blank">メタデータを理解する</a>（制作基本チュートリアル）

<blockquote>
ユニーク識別子は，出版物を特定するための一意の識別子であり，他の出版物と重複しない値を指定します．この識別子には，UUID, DOI, ISBNやISSNなどが利用されます．
</blockquote>

Harogomoでは、自動的にIDを割り当ててくれるので、あまり気にしないでもよいでしょう。そういうものがある、ぐらいに理解してください。

５）言語は、日本語なら縦書きであろうが横書きであろうが「ja（日本語）」でOKです。

６）カバーイメージは、表紙ですね。ここにドロップした画像ファイルが表紙になります。

７）続いてアウトラインに関する項目が二つ出てきますが、これは後でまとめてやりましょう。

８）最後に「出版社」「出版日付」「著作権」「説明」が入力できます。

※いろいろ入力したところ。
<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot14.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot14.png" alt="screenshot" width="382" height="521" class="alignnone size-full wp-image-13374" /></a>


<H3>構成とアウトライン</H3>

原稿データを作る上で気をつけておきたいのが、先ほどの「アウトライン」です。項目は二つありました。

<ul>
	<li>アウトライン[レベルx]の内容を目次として使う</li>
	<li>アウトライン[レベルx]の前で改ページする</li>
</ul>

ともに[レベルx]に選択できるのは、

レベル０
レベル０ー１
レベル０ー２

の３つです。

アウトラインに慣れない人にはわかりにくいと思いますので、目次の場合で考えてみましょう。

レベル０とは、経験値が全く貯まっていない状態ではなく、アウトラインの階層で一番上のものを指します。つまり、どこの子でもない要素ですね。レベル０を選択した場合は、それらの要素が目次として使われます。０ー１であれば、レベル１も含めたもの、さらに０ー２であればレベル２まで含まれます。

たとえば、エッセイ集のような構成なら「レベル０」を選択すれば問題ありません。

<strong>エッセイ１　→レベル０
　本文　　　→レベル１
エッセイ２
　本文
エッセイ３
　本文</strong>

※「エッセイ１」「エッセイ２」「エッセイ３」が目次に使われる。

もし、章立てがあり、節もあるなら、「レベル０ー１」がよいでしょう。

<strong>第一章　　　　　→レベル０
　セクション１　→レベル１
　　本文　　　　→レベル２
　セクション２
　　本文
第二章
　セクション１
　　本文
　セクション２
　　本文</strong>

※「章」と「セクション」が目次に使われる。

さらに大がかりで、章の上に部があるなら「レベル０ー２」です。

<strong>第一部　　　　　　→レベル０
　第一章　　　　　→レベル１
　　セクション１　→レベル２
　　　本文　　　　→レベル３
　　セクション２
　　　本文
　第二章
　　セクション１
　　　本文
　　セクション２
　　　本文
第二部
　第三章
　　セクション１
　　　本文
　第四章
　　セクション１
　　　本文</strong>

※「部」「章」「セクション」が目次に使われる。

改ページについても、同じ理解で問題ありません。もちろん、「アウトライン[レベルx]の前で改ページする」を使わずに、メニューの「編集」から「改ページを挿入」を選択して、細かくコントロールすることもできます。ただし、本文が多いと面倒なので、この制御方法も覚えておくとよいでしょう。

<H3>目次と本文</H3>

では実際に「部・章・セクション」構成でEPUBファイルを作ってみましょう。

以下のようなファイルを、EPUB出力してみます。選択するのは「レベル０ー２」。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot16.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot16.png" alt="screenshot" width="450" height="216" class="alignnone size-full wp-image-13376" /></a>

完成したファイルをiBooksでチェック。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot17.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot17.png" alt="screenshot" width="443" height="469" class="alignnone size-full wp-image-13377" /></a>

どやら目次はうまくできたようです。しかし、問題が発生しました。次は本文の画面。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot18.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot18.png" alt="screenshot" width="435" height="161" class="alignnone size-full wp-image-13378" /></a>

アウトラインの「子」に当たる要素を示す「・」が本文中にも登場しています。さすがに見た目が悪いですね。

これはメニューの「アウトライン」→「デフォルトリスト設定」で制御できます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot19.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot19.png" alt="screenshot" width="434" height="279" class="alignnone size-full wp-image-13379" /></a>

ここでレベル１〜レベル５までのリストの表示をカスタマイズ可能。デフォルトでは「・」になっているので、それを「＜space＞」に変更すれば、以下のように、頭の記号を消せます。

※通常のリストとspaceに変えたリスト
<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot20.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot20.png" alt="screenshot" width="257" height="116" class="alignnone size-full wp-image-13380" /></a>

ただし、一度入力されたリストには、この設定は反映されないようなので、文章を作成する前にリスト表示を設定しておきましょう。文章を入力し終えてから、リストの表示を変更しようと考えていると悲劇が起きます。
※コンテキストメニューから「リストマーク」の変更は可能ですが、現状一行ずつしか変えられないようです。

その点にさえ注意しておけば、特に問題はないでしょう。

<H3>ちなみに話</H3>

ちなみに、最初に設定した情報は、「epd.opf」（※）というファイルで以下のようなメタデータとして使用されます。
※EPUBを解凍すると見えます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot21.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot21.png" alt="screenshot" width="307" height="188" class="alignnone size-full wp-image-13381" /></a>

また、本文回りのHMTLは次のような感じでした。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot22.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot22.png" alt="screenshot" width="500" height="76" class="alignnone size-full wp-image-13382" /></a>

CSSをいじってやろうという感じの方はご参考程度に。

<H3>さいごに</H3>

ポイントは二つ。

<ul>
	<li>アウトラインを使って、本の構成を制御する</li>
	<li>本文を書く前に「・」を「＜space＞」にしておく</li>
</ul>

これだけです。ただ、前回も書きましたがCSSが非常にシンプルなので、後から自分でカスタマイズする必要があるかもしれません。

また、＜H＞タグが使えませんし、太字にしても＜STRONG＞が割り当てられるわけでもありません。＜SPAN＞による太字表現と、＜STRONG＞による太字表現は、厳密には違うものです。その意味でEPUBエディタとしては、やや力不足な点はあるでしょう。今のところは。

今後、EPUBを書き出す際の変換をユーザーが（ある程度）制御できるようになるなら、また違った使い勝手が生まれてくるかもしれません。あるいは、そういうスクリプトを書くとか……。とりあえず、今後に期待です。

<strong>▼関連エントリー：</strong>
<a href="https://rashita.net/blog/?p=13393" target="_blank">Hagoromoの文章をEvernoteに保存するスクリプト</a>