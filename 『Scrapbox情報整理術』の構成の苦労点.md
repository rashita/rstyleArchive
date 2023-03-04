---
title : 『Scrapbox情報整理術』の構成の苦労点
link : 25400
date : Thu, 16 Aug 2018 02:41:46 +0000
categories : ["writingmethod"]
tags : ["scrapbox","本の作られ方"]
draft : false
author : 倉下忠憲
---

<a href="https://scrapbox.io/scrapbox-drinkup/%E3%80%8EScrapbox%E6%83%85%E5%A0%B1%E6%95%B4%E7%90%86%E8%A1%93%E3%80%8F%E5%88%B6%E4%BD%9C%E7%A7%98%E8%A9%B1(rashita)">『Scrapbox情報整理術』制作秘話(rashita) - scrapbox-drinkup</a>

で話したことを、記事にも起こしておきます。

■

Scrapboxを最初に触ってみて、最初に驚いたのが「操作が簡単だ」ということでした。ややこしい概念の説明なくても、すぐさまページを作り、入力を進めていけます。インターフェイスもシンプルで、ボタンなども非常に少ないものです。

つまり、基礎的な話で言えば、その説明は非常に分量が少ないのです。

一方で、本格的に使い込むと、途端に話がややこしくなります。細かい機能はわんさかありますし、しかも上級編であるUserScriptとUserCSSはそれぞれJavaScriptとCSS(+HTML)の知識を使います。がっつりWebデザインの領域です。

仮にそれを図示するとしたら、以下のようになるでしょう。

<a href="https://gyazo.com/8908ddc9b654e72103d5f67c70e5b406"><img src="https://i.gyazo.com/8908ddc9b654e72103d5f67c70e5b406.png" alt="Image from Gyazo" width="930"/></a>

縦が習熟度で、左右が必要な知識の量です。下に行くほど、急激に知識の量が増える。そういう本の解説書を書かなければならない、という状況に陥ったわけです。

言い換えれば、「解説書が必要ないくらい簡単に使い始められるツールの解説書」であり、かたや「真剣に解説しはじめると本一冊ではとても足りないくらい知識が必要なツールの解説書」なわけです。なんとなく難易度は伝わるでしょうか。どこまで書いて、どこまでは書かないか。そういうジャッジメントが必要でした。

■

さらに、です。話の組み立て方も難しさがありました。

おおよそこの手の解説書には、二つの進め方があるかと思います。

一つは、機能の階段方式で、一番簡単な機能からスタートし、徐々に難しい機能へと網羅的に進んでいくアプローチです。よくある方式ですが、これをScrapboxでやると、序盤がすさまじく詰まらなくなります。だって、「解説書が必要ないくらい簡単に使い始められるツール」なわけですから。Webブラウザを触ったことがある人間なら、一目見て分かる操作を延々と説明し続けなければなりません。私の直感では、そういう本は間違いなく面白くありません。退屈でページを閉じられてしまった時点で書き手の負けです。

だったら、もう一つのチュートリアル方式はどうでしょうか。使い始めたばかりのユーザーとまったく同じ立場になり、「最初にプロジェクトを作りましょう。次に、この操作でページを作ります」のように、手順ベースで説明を進めていく方式です。一応私は、この方式を念頭において最初に構成案を立てていました。しかし、書き進めていくうちに問題が発生したのです。

Scrapboxの、使い勝手の良さは「予測のリンクと不測のリンク」にあります。

予測のリンクは、すでに自分がそのページをあることがわかっていて、今書いているページとリンクをつなげたいと思うもの。以前自分はこれについて書いていたな、というおぼろげな記憶と、その内容に関するタイトルの一部分を思い出せば、そうしたページにリンクをちゃちゃっとつけられるのがScrapboxの素晴らしいところです。

しかし、チュートリアル方式では、それが作れません。なぜなら、一つひとつ手順を追っておくやり方では、そのプロジェクトはまったく真っ白な状態であり、他にページが存在しないからです。

かと言ってです。まずAというページを作り、その後Bというページを作っているときに[A]みたいなリンクを追加しましょう、というのでは「予測」でもなんでもありません。お膳立てしているだけです。Scrapboxを使っているときに感じる快適さは、そういうお膳立てがないところで、ちゃちゃっとリンクが作れるところなので、あまりにも作為的というか不自然な状況になってしまいます。

もう一つの不測のリンクについても同じことが言えます。不測のリンクとは、ページを書いているときに目についたキーワードをリンク化したときに、そんなページとつながるとは思っていなかったページが関連ページに表示されることです。これも他にページがない状況では発生しようがありませんし、Aを作ってBを、みたいなやり方でも──なにせ何を作ったのか覚えているわけですから──機能しません。

ようするに、上記のような構成案は、話としては破綻しないものの、Scrapboxの「良さ」を完全に伝えきれないな、と判断したわけです。

■

そこからが苦労の連続でした。では、どうしたら面白く読めて、Scrapboxの良さを伝えられるのか。書く内容そのものはたいして変えずに、その順番をさまざまに試しました。

で、できあがったのが現在の目次案です。

■コンテンツ
●PROLOGUE ようこそScrapboxへ
●CHAPTER-1 Scrapboxの構成と入力方法
●CHAPTER-2 Scrapboxはネットワーク構造で情報を整理する
●CHAPTER-3 Scrapboxで知をつないでいく
●CHAPTER-4 もっと便利にScrapboxを使う
●EPILOGUE 知のコラボレーションで時代を切り開く

この流れに込められた意図なども解説しようかと思いますが、長くなってきたので、今回はここまでとしておきます。

<strong>▼新刊発売中：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863542526/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51L7tTg9PML._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863542526/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.08.16</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2018-07-27)<br />売り上げランキング: 12,118<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863542526/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
