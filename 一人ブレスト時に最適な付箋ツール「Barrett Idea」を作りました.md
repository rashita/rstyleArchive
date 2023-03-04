---
title : 一人ブレスト時に最適な付箋ツール「Barrett Idea」を作りました
link : 14634
date : Thu, 23 Oct 2014 02:09:55 +0000
categories : ["0-知的生産の技術"]
tags : ["barret-idea","考具"]
draft : false
author : 倉下忠憲
---

というか完全に自分用ですし、β版の45歩ぐらい手前のバージョンですが。

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot36.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot36-1024x667.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-14635" /></a>

制作はHTML5 + Javascript。つまり単なるウェブページです。ドラッグによる移動は<a href="http://jquery.com/" target="_blank">jQuery</a>および<a href="http://jqueryui.com/" target="_blank">jQuery UI</a>にて実装しております。

<H3>動作説明</H3>

操作はビビるほど簡単です。テキストエリアに文字を入力し、

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot37.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot37.png" alt="screenshot" width="250" height="174" class="alignnone size-full wp-image-14636" /></a>

タンっ！とリターンキーを押すだけ。

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot38.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot38.png" alt="screenshot" width="251" height="137" class="alignnone size-full wp-image-14637" /></a>

すると付箋が一つできます。あとは、もうこれをただひたすら繰り返していくだけです。

画面上の付箋は、ドラッグで移動可能。本当に、機能はこれだけです。

<H3>簡単な使い方</H3>

使い方としては、まず付箋を大量に作る。頭の中を出し切る感じで付箋を作る。テキストを入力してリターン、テキストを入力してリターンと、シンジくんのようにぶつぶつ言いながら付箋を生み出していきます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot39.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot39.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14638" /></a>

で、出し終えたら、それらをドラッグして並び替え、近しいものを集めていったり、階層を作ったりします。

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot40.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot40.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14639" /></a>

以上。

とにもかくにも付箋を作るときの操作をシンプルにするように努めました。アイデア出しを行う際は、一手間や二手間が非常に邪魔になってきます。それをシンプルにそぎ落とした付箋ツールです。

あまりにシンプルなので、作った付箋を削除することもできません。邪魔な付箋はページの下に移動させるぐらいしか打つ手無しです。ちなみに、ページをリロードすると、すべての付箋が消え去ります。諸行無常です。

<H3>ダウンロード</H3>

こんな貧相なものでよろしければ、以下からダウンロードください。

<a href="https://www.dropbox.com/s/wwypwcdgly2yrmm/BarrettIdea.zip?dl=0">BarrettIdea.zip</a>

zip解凍後のHTMLを開いてもらえばOKです。ウェブブラウザさえあれば動きます。もちろん、ウェブブラウザ上で動きます。

ただし、MacのFirefoxにしか最適化していないので（私の環境です）、それ以外のブラウザとかWindowsでどうなのかはわかりませんのであしからず。

基本的に青色は正義ですが、こんな付箋の色はいやじゃい、という方はhtmlファイルのCSS指定を変えてください。

<a href="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot41.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/10/screenshot41.png" alt="screenshot" width="439" height="289" class="alignnone size-full wp-image-14640" /></a>

background-colorのカラーコードを変えれば付箋の色が変わります。



<H3>さいごに</H3>

もう少し機能を増やすとすれば、

・付箋の色を選択できるようにする
・ゴミ箱の設置
・まとめたものをテキストで出力

というところでしょうか。

アルゴリズムは思いつきますが、実装する時間が……。