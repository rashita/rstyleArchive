---
title : Scrivenerで見出し部分だけを出力して、目次っぽいファイルを作る
link : 11505
date : Wed, 25 Sep 2013 04:40:06 +0000
categories : ["scrivenerへの散歩道"]
tags : ["scrivener"]
draft : false
author : 倉下忠憲
---

統合執筆環境ツールであるScrivenerには多様な出力形式があります。

その中の一つに「Synopses and Titles」というものがあり、これを使えば見出し部分だけを抽出したファイルを作成可能です。ようするに目次を作成できるということ。

実際にやってみましょう。

<H3>Let' Try!</H3>ちょうど、いま進めているプロジェクトファイルがありましたので、それを使います。

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot23.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot23.png" alt="screenshot" width="500" height="512" class="alignnone size-full wp-image-11506" /></a>

章にあたるフォルダと、その内容に当たるノート、という二階層の構造になっています。
※この形でないといけない、というわけではありません。

さっそく「Compile」ボタンを押してみましょう。上部のツールバーにある、青い矢印＋書類のアイコンです。

画面が表示されたら、上部の「Format As」を「Synopses and Titles」に変更し、ウィンドウ下部の「Compile For」を「Plain Text(.tx)」変更。

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot25.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot25.png" alt="screenshot" width="500" height="442" class="alignnone size-full wp-image-11508" /></a>

後は「Compile」をクリックするだけ。

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot26.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot26.png" alt="screenshot" width="500" height="763" class="alignnone size-full wp-image-11509" /></a>

このような見出し部分だけを抽出したテキストファイルが出来上がります。まったくもって目次ですね。

しかし、よく見ると「Section」の部分が二回出てきています。これは私のプロジェクト構造の作り方に問題があるわけですが、いちいち構造を手直しするのも面倒くさい。そこで、Compileのオプション設定をいじることで対応してみます。

もう一度ツールバーから「Compile」ボタンをプッシュ。その後、左サイドバーの「Formatting」をクリック。

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot27.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot27.png" alt="screenshot" width="500" height="442" class="alignnone size-full wp-image-11510" /></a>

ここではどのレベルの階層を表示するのか（あるはしないのか）を設定できます。

個別のファイルについてのオン・オフは「Contents」で制御できるのですが、こちらは「第三階層のノートのタイトルは表示しない」といった構造に対応した制御が可能です。もちろん「Title」だけは表示して、「Synopses」は表示しない、という使い方もできます。

とりあえず、今回は第一階層のフォルダの表示を切ってみましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot28.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot28.png" alt="screenshot" width="500" height="442" class="alignnone size-full wp-image-11511" /></a>

チェックボックスを外しました。

この状態でCompileすると、

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot29.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot29.png" alt="screenshot" width="449" height="766" class="alignnone size-full wp-image-11512" /></a>

と、第一階層のフォルダ名が省略された形でテキストファイルができあがっております。

このように柔軟な指定ができるので、自分の好きなようにプロジェクト構造を作り、それに合わせて見出しを出力することが可能です。

<H3>Synopses</H3>今回は目次作りをイメージしたので、「Synopses」については省略しました。「Synopses」はそのノート（あるいはフォルダ）の概要を示すものです。

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot30.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot30.png" alt="screenshot" width="500" height="105" class="alignnone size-full wp-image-11513" /></a>

この右側に表示されているものが「Synopses」。ここに入力しておけば、

<a href="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot31.png"><img src="https://rashita.net/blog/wp-content/uploads/2013/09/screenshot31.png" alt="screenshot" width="433" height="205" class="alignnone size-full wp-image-11517" /></a>
当然のようにテキストファイルにも出力されます。

「Synopses」を入力したけれども、それを含めたくない場合は、「Formatting」で制御すればよいのでしたね。また第一階層の「Synopses」だけは表示させる、という使い方も可能。使い方はあなた次第、という陳腐な文句を心の底から使いたくなってくる柔軟性の高さです。

<H3>さいごに</H3>今回はテキストファイルでやりましたが、もちろんPDF形式での出力も可能です。

その場合、「Contents」の「Pg Break Before」のチェックマークを全てオフにしておきましょう。でないと、見出しごとに1ページが出来上がるというなんとも贅沢なPDFになってしまいますので。

今回は、以上です。皆様のScrivenerライティングライフにご加護がありますように。

<h2><span style="color: rgb(0, 0, 255);">Scrivener</span></h2><div style="margin: 0;float: left;"><div style="margin-left: 109px;"><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" rel="nofollow" style="text-decoration: none;"><img src="http://a375.phobos.apple.com/us/r1000/068/Purple/v4/7f/c7/66/7fc7663d-0b33-0fcb-7924-d384ce39b2a5/Scrivener.100x100-75.png" style="margin-left: -109px; float: left; width: 100px; height: 100px;"><img src="http://r.mzstatic.com/htmlResources/2338/images/mask100.png" style="margin-left: -109px; float: left; width: 100px; height: 100px;" /></a></div></div> カテゴリ: 仕事効率化, 教育<br><br> 販売元: <a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" rel="nofollow">Literature & Latte - Literature & Latte Ltd</a><br> リリース日: 2011/07/06<br style="clear: both;">