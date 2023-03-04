---
title : 「Milanote」のExport機能
link : 19808
date : Tue, 31 Jan 2017 02:25:20 +0000
categories : ["物書き生活と道具箱"]
tags : ["milanote"]
draft : false
author : 倉下忠憲
---

前回：<a href="https://rashita.net/blog/?p=19792">「Milanote」のBoard機能で階層を作る</a>

今回は「<a href="http://milanote.com/">Milanote</a>」のExport機能についてみていきます。残念ながら、現段階では一番残念な機能です。

<h3>Exportの種類</h3>

作成したボードを外部出力するための「Export」機能には、いくつかのフォーマットが選択可能です。簡単に見ていきます。

■PDF（Canvas）

<a href="https://rashita.net/blog/?attachment_id=19809" rel="attachment wp-att-19809"><img src="https://rashita.net/blog/wp-content/uploads/2017/01/screenshot40-500x278.png" alt="screenshot" width="500" height="278" class="alignnone size-medium wp-image-19809" /></a>

配置したパーツをそのままに画像形式でPDF化。ちなみに現状では、日本語はバケます。

■PDF

<a href="https://rashita.net/blog/?attachment_id=19810" rel="attachment wp-att-19810"><img src="https://rashita.net/blog/wp-content/uploads/2017/01/screenshot41-500x394.png" alt="screenshot" width="500" height="394" class="alignnone size-medium wp-image-19810" /></a>

テキストに起こしたPDF。こちらも日本語はバケます。

■Word

<a href="https://rashita.net/blog/?attachment_id=19811" rel="attachment wp-att-19811"><img src="https://rashita.net/blog/wp-content/uploads/2017/01/screenshot42-500x545.png" alt="screenshot" width="500" height="545" class="alignnone size-medium wp-image-19811" /></a>

WordやPagesで読み込めるdocx形式での出力。こちらはきちんと日本語が通ります。

■Markdown

<a href="https://rashita.net/blog/?attachment_id=19812" rel="attachment wp-att-19812"><img src="https://rashita.net/blog/wp-content/uploads/2017/01/screenshot43-500x514.png" alt="screenshot" width="500" height="514" class="alignnone size-medium wp-image-19812" /></a>

見出しや他のテキスト装飾がマークダウン変換されたmdファイル形式。

■plaintext

<a href="https://rashita.net/blog/?attachment_id=19813" rel="attachment wp-att-19813"><img src="https://rashita.net/blog/wp-content/uploads/2017/01/screenshot44-500x594.png" alt="screenshot" width="500" height="594" class="alignnone size-medium wp-image-19813" /></a>

ごくシンプルなプレーンテキストで、階層表現が行頭のスペースで表現されています。

<h3>イマイチな出力機能</h3>

というわけで、まず日本語環境ではPDFはどちらも使えません。この辺は徐々に改善されるでしょう。あるいはそれに期待です。

少し使いづらいのは、どれか特定のボードだけを選んで出力、というのが不可能な点です。現状では、すべての階層が一枚のファイルとして出力されます。これは選択できるのが望ましいです。

で、ややこしいのが階層表記です。かなり癖のある見出しの処理をしてくれます。マークダウンで考えてみましょう。

<a href="https://rashita.net/blog/?attachment_id=19814" rel="attachment wp-att-19814"><img src="https://rashita.net/blog/wp-content/uploads/2017/01/screenshot45-500x267.png" alt="screenshot" width="500" height="267" class="alignnone size-medium wp-image-19814" /></a>

こういうボードが、以下のように見出し付けされます。

<a href="https://rashita.net/blog/?attachment_id=19815" rel="attachment wp-att-19815"><img src="https://rashita.net/blog/wp-content/uploads/2017/01/screenshot46-500x514.png" alt="screenshot" width="500" height="514" class="alignnone size-medium wp-image-19815" /></a>

冒頭の「# tadanori's workspace」はいいですね。次の「## 月刊くらした計画」も構いません。ややこしいのが、その次の「# 月刊くらした計画」です。階層が一つ上に戻っています。さらにその次の「# 月刊くらした計画ZZ」で、見出し１のレベルが連続しています。さて、これはどのように解釈すればよいのでしょうか。

整理してみると、まずボードそのものの名前は#で見出し付けされます。そして、そのボードに含まれるコラムが##で見出し付けされます。また、ボードに配置されたNote（テキスト要素を扱うパーツ）で設定した見出しは###で処理されます。

ここまではわかりやすいですね。では、ボードに配置されたボードはどうなるかというと、「ボードそのものの名前は#で見出し付けされる」が適用されて、#になるのです。だからもしメインのボードに１つだけボードを配置し、そのボードの中にまた1つだけボードを配置しを繰り返していくとひたすらに#の見出しが並ぶことになります。

これは将来的にボードを選択して出力する事態を見越しているのか、あるいは階層が深くなりすぎると#が７つ以上になってしまう事態を回避しているのかはわかりませんが、とにかく何かしらは理由があるのでしょう。とはいえ、若干扱いが面倒ではあります。

ちなみに「Unsorted notes」に入れてあるものも、きちんと末尾に配置されて出力されます。これはあるいは出力されない方が使い勝手がよいのかもしれません。

<h3>さいごに</h3>

というわけで、作成の面ではいろいろ気配りが聞いたツールではありますが、現状の段階でのExport機能はそれほど当てになるものでも、小回りが利くものでもありません。一応プレーンテキストであれば行頭のインデントがあるので、WorkFlowyなんかには投げやすいかもしれません。

とりあえず、全体的に改善の期待が強い機能回りです。


