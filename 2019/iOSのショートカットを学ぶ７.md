---
title : iOSのショートカットを学ぶ７
link : 28598
date : Sun, 16 Jun 2019 22:00:10 +0000
categories : ["プログラミング"]
tags : ["ios","iosショートカット"]
draft : false
author : 倉下忠憲
---

前回：<a href="https://rashita.net/blog/?p=28584">iOSのショートカットを学ぶ６</a>

前回は、入力したテキストの一行目だけを取り出すことに成功した。ただ、その手順を踏んでしまうと、今度は本文全体がスムーズには取り出せなくなる。

どうするか？

<h2>変数の設定</h2>

やり方はいろいろあるだろうが、今回は「変数」を活用してみる。

まず、一行だけ取り出したものを、Titleという変数に入れる。入れ方は、検索ボックスに「変数」と入力し、「変数の設定」を探した上で、それを設置する。

<a href="https://rashita.net/blog/?attachment_id=28600" rel="attachment wp-att-28600"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/FB3BC0B5-6443-40FC-B041-FB9830DA1B35.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28600" /></a>

<a href="https://rashita.net/blog/?attachment_id=28601" rel="attachment wp-att-28601"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/3237374D-D6DE-40E2-9396-16CDB3A12FAD.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28601" /></a>

でもって、変数名に「Title」と入れる。この名前は恣意的なものなので、別に他の名前でも構わない。極端なことを言えば、fqu31nfwfq11のようなパスワード用の文字列みたいなのだってヘッチャラである。が、後から「あれ？　これ何入れてたんだっけ？」みたいなことになりやすいので、中身がすぐわかる名前にしておくのが賢明である。

<a href="https://rashita.net/blog/?attachment_id=28602" rel="attachment wp-att-28602"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/571340B1-5AFD-4F03-9876-5B30A51E2FFC.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28602" /></a>

とりあえず、このアクションの設置で、取り出した一行目が「Title」という変数に入った。が、これだけではまだ本文は使えない。よって、もうワンステップ挟む。

<h2>変数の取得</h2>

同じく検索ボックスに「変数」と入れ、今度は「変数の取得」を設置する。

<a href="https://rashita.net/blog/?attachment_id=28603" rel="attachment wp-att-28603"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/1C23752F-FC6E-4DC4-A6B9-569B5EFD4E35.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28603" /></a>

ご覧のようにデータの流れが一度途切れているのがわかるだろう（真ん中の線が切れている）。これがポイントだ。で、項目にある「変数の選択」を押すと、次のような選択肢が出てくる。

<a href="https://rashita.net/blog/?attachment_id=28604" rel="attachment wp-att-28604"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/2EA62285-3BB3-475A-B573-A0F0F9183C8A.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28604" /></a>

「title」を取得しても意味がないので、選ぶのは「マジック変数を選択」の方だ。すると、以下のような画面になる。

<a href="https://rashita.net/blog/?attachment_id=28605" rel="attachment wp-att-28605"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/FAED69A9-802E-4BB0-A05B-2509FFD30A34.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28605" /></a>

アクションとアクションの間にボタンが増えている。でもって、それを押すと、直前のアクションのデータが取得できる。これが「マジック変数」の強力なところだ。どこが強力なのかというと、普通のプログラミングでは先ほど出てきたようにイチイチ変数を作りそこにデータを入れておかないと、再利用ができないのだが、この「マジック変数」であれば、任意の段階のデータを簡単に引っ張ってこれる。非常に楽チンだ。

まあ、難しい話はさておいて、ここで必要なのは本文となるデータであり、それはつまり何の加工も施されていない、「入力を要求」を終えたばかりのデータということになる。なので「入力を要求」を押す。

<a href="https://rashita.net/blog/?attachment_id=28606" rel="attachment wp-att-28606"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/4AE6799B-C857-44C0-8F15-ACA741D52915.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28606" /></a>

これで、このアクションには本文データが入っている。あとは、簡単だ。一番最初にやったように、このデータにEvernoteの新規作成アクションを繋げればいい。

<a href="https://rashita.net/blog/?attachment_id=28607" rel="attachment wp-att-28607"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/EB7F583C-DDE1-46D8-B859-919E53BDAB54.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28607" /></a>

でもって、「ノートタイトル」の部分には、先ほど作成した「Title」という変数を指定すればOKだ。

<a href="https://rashita.net/blog/?attachment_id=28608" rel="attachment wp-att-28608"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/96DAA695-556F-465D-A89F-FB2D312C10BD.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28608" /></a>

<h2>実践</h2>

では、実際にやってみよう。

<a href="https://rashita.net/blog/?attachment_id=28609" rel="attachment wp-att-28609"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/8FC261EA-E6ED-4348-A57B-D27313DD18A7.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28609" /></a>

<a href="https://rashita.net/blog/?attachment_id=28610" rel="attachment wp-att-28610"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/screenshot-4.png" alt="" width="616" height="437" class="alignnone size-full wp-image-28610" /></a>

きれいに一行目だけがタイトルとなり、本文にはすべての行が入っている。完璧だ。

というように、変数をうまく使えば、データを必要なタイミングで持ってくることができる。これはぜひ覚えておきたい方法である。

ちなみに、勘の良い方は気がついたかもしれないが、「マジック変数」を使えば、実は最初の「変数の設定」は飛ばすことができる。つまり、以下のようにノートタイトルの指定にすら「マジック変数」を使えばまったく同じ動きになる。

<a href="https://rashita.net/blog/?attachment_id=28611" rel="attachment wp-att-28611"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/DDBA8A44-A105-43B6-A8D6-7852CD222F3E.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28611" /></a>

が、今回は「変数」という概念を掴まえて欲しかったので、あえて設定してみた。非常に単純な処理の場合はマジック変数で問題ないだろうが、そうでない場合もあるだろうし、それに備えて学んでおくのは悪くないだろう。

というわけで、これで簡素な「FastEverもどき」は一応完成である。

次回は、このアレンジバージョンを作ってみよう。