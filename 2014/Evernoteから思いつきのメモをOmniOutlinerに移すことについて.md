---
title : Evernoteから思いつきのメモをOmniOutlinerに移すことについて
link : 12559
date : Wed, 29 Jan 2014 04:15:27 +0000
categories : ["evernoteの使い方"]
tags : ["evernote","omnioutliner"]
draft : false
author : 倉下忠憲
---

先日、「<a href="http://www.omnigroup.com/omnioutliner/" target="_blank">OmniOutliner 4</a>」の試用版をダウンロードしました。Macで使えるクールなアウトライナーです。

<span class="appIcon"><img class="appIconImg" height="60" src="http://a3.mzstatic.com/us/r30/Purple/v4/e7/00/bc/e700bc0b-527c-0bae-471a-ea1275d7053b/OmniOutliner.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/omnioutliner/id404478020?mt=12&uo=4&at=11l4y8" target="itunes_store">OmniOutliner</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, ビジネス</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/omnioutliner/id404478020?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;@media only screen{background-image:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.svg);}"></a></span><br style="clear:both;">

「AppleScriptが使えるよ」と説明があったので、ちょっと思いつきました。

「Evernote→OmniOutliner4」のスクリプトがあれば面白いんじゃないか、と。

一度思いついてしまうと、作らずにはいられません。試行錯誤（※）を重ねて、ベータ版ができました。
※以下のリンクから、作成の登山ルートが確認できます。

<a href="http://rashita.hatenablog.com/entry/2014/01/28/150947" target="_blank">EvernoteからOmniOutlinerに放り込むアプリが一応できたよ【AppleScript】</a>（ジャムスタ）

自分で作ったアプリなのですが、使ってみて「そうだ、こういうことをやりたかったのだ」と、改めて確認することになりました。

Evernoteは記憶のツールであって、思考のツールではありません。

きちんと役割分担が必要です。

<H3>検索で掘り出せるもの</H3>一番最初の形は、「自分で選択したノートを、そのタイトルをトピックにしてアウトライナーに放り込む」というものでした。実装は簡単で、機能も「まあ、こうだろうな」と思う範囲です。

「おや？」と思い始めたのは、検索してその結果をアウトライナーに放り込むようになってから。なにかよくわからない感覚が生まれてきました。もうちょっと、機能を作り込んでみよう。そう思って、ノートブックを選択できるようにしました。あと、タグ選択も可能に。

完成したベータ版を使ってみたところ、何とも言えない感覚が沸いてきました。

アプリを使い、「アイデアノート」ノートブックを「情報カード」で検索した結果がこれです。

<a href="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot7-1024x668.png" alt="screenshot" width="500" height="330" class="alignnone size-large wp-image-12560" /></a>

少しノイズが混じっているので、それを除去します。

<a href="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot8-1024x668.png" alt="screenshot" width="500" height="330" class="alignnone size-large wp-image-12561" /></a>

こうなりました。これらは全て私のノートなので、他の人が見ても特に思うところはないかもしれません。しかし、私がこのリストを見ると、いろいろ思いつくのです。

<H3>記憶→思考</H3>ノートを選択してアウトライナーに放り込む、というのは、「意識」の範囲内の行為です。

しかし、すでに私の「アイデアノート」ノートブックには3000を超えるノートがあり、文脈も入り交じっています。その全てを精査することは難しいでしょう。

しかし「検索」であれば事情は違います。「そうだ、こういうノートもあったな」といったものが掘り起こされます。そして、それは単に掘り起こされるだけではないのです。アウトライン上に並び、入れ換えたり、階層構造を生み出したりすることができます。

思考の準備が整っているのです。

<H3>アウトライナーの使い方</H3>アウトライナーについてもう少し書いてみます。

これまでの私のアウトライナーの使い方は、たとえば「ブレスト」です。

考えたい項目のトピックを作り、その下に思いつくままに書き出していく。それを入れ換えたり、入れ子にしたりしながら、アイデアの形を整えていく。そんな使い方です。

あるいは、アイデアだし自体は他のツール（たとえば付箋とペン）で行い、その結果をアウトライナー上でまとめる、なんて使い方もします。アウトライナーは要素が一直線上に並ぶので、文章化の準備にぴったりなのです。

これらは、何かしらの目的があって書き出したものをまとめた、と表現できるでしょう。

これとは違う使い方ができないかな、と以前から考えていました。

たとえばTwitterの一つのつぶやきをアウトライナーの１トピックにして、それらを操作できないかな、といったアイデアです。Twitterのつぶやきは、何かしらの目的で統一されたものではありません。ほんとうに散漫な思いつきです。でも、私の思いつきでることには違いありません。

それらを操作して思考の材料にすることができれば、きっと面白いだろう、と思いました。何がどう面白いのかはわからないが、面白いに違いない、という直感です。

幸い、私のEvernoteの「アイデアノートブック」は、一行だけの書き込み（※）など、Twitterのつぶやきとほとんど変わらないものが並んでいました。実験にぴったりです。
※ノートタイトル＝ノートの中身

<H3>メモから発想する</H3>先ほどのリストをもう一度ご覧ください。

※拡大版
<a href="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot9.png" alt="screenshot" width="500" height="605" class="alignnone size-full wp-image-12562" /></a>

全然関係ない要素ですが、「Evernoteにカードを作れるアプリ」「間違ったKJ法」「ビジネスパーソンが学ぶべきこと」が並びました。ここから、新人ビジネスパーソン向けのKJ法を学べるEvernoteと連携するカードアプリ、なんてアイデアが生まれてきます。

ここでのポイントは、そういうアイデアを出そうと思ってアウトラインに並べたわけではない、という点です。

いろいろ操作してアウトラインはこんな感じになりました。

※操作後
<a href="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot10.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/01/screenshot10.png" alt="screenshot" width="500" height="602" class="alignnone size-full wp-image-12563" /></a>

アウトプットの素材になりそうなものが、いくつもできそうです。

<H3>さいごに</H3>Evernoteを使い始めたころの自分から、今の自分に至るまでに積み上げてきた地層があり、その中で有機的な化学反応が起きる。というと、少々大げさかもしれません。

しかし、単に想起するだけでなく、それらを入れ換え、組み替え、構造化することで、新しい何かを生み出せることはありそうです。

もちろん、これは「何をEvernoteに残しているか」によって変わってきます。私の場合は「一行メモ」が多いので、アウトライナーとの親和性が高かったのです。

<strong>▼こんな一冊も：</strong>
<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/Evernote%E3%81%A8%E3%82%A2%E3%83%8A%E3%83%AD%E3%82%B0%E3%83%8E%E3%83%BC%E3%83%88%E3%81%AB%E3%82%88%E3%82%8B-%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E7%99%BA%E6%83%B3%E8%A1%93-%E3%83%87%E3%82%B8%E3%82%BF%E3%83%AB%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4774151505%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4774151505" target="_top">Evernoteとアナログノートによる ハイブリッド発想術 (デジタル仕事術)</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/Evernote%E3%81%A8%E3%82%A2%E3%83%8A%E3%83%AD%E3%82%B0%E3%83%8E%E3%83%BC%E3%83%88%E3%81%AB%E3%82%88%E3%82%8B-%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E7%99%BA%E6%83%B3%E8%A1%93-%E3%83%87%E3%82%B8%E3%82%BF%E3%83%AB%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4774151505%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4774151505" target="_top"><img src="http://ecx.images-amazon.com/images/I/41kEDq5iQ6L._SL160_.jpg" border="0" alt="Evernoteとアナログノートによる ハイブリッド発想術 (デジタル仕事術)" /></a></td><td valign="top"><font size="-1">倉下 忠憲 <br /><br />技術評論社  2012-06-30<br />売り上げランキング : 102221<br /><br /><br /><a href="http://www.amazon.co.jp/Evernote%E3%81%A8%E3%82%A2%E3%83%8A%E3%83%AD%E3%82%B0%E3%83%8E%E3%83%BC%E3%83%88%E3%81%AB%E3%82%88%E3%82%8B-%E3%83%8F%E3%82%A4%E3%83%96%E3%83%AA%E3%83%83%E3%83%89%E7%99%BA%E6%83%B3%E8%A1%93-%E3%83%87%E3%82%B8%E3%82%BF%E3%83%AB%E4%BB%95%E4%BA%8B%E8%A1%93-%E5%80%89%E4%B8%8B-%E5%BF%A0%E6%86%B2/dp/4774151505%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3D4774151505" target="_top">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>

