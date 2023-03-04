---
title : 情報管理ツール：7wrinerについて　その１
link : 23282
date : Wed, 08 Nov 2017 02:19:25 +0000
categories : ["断片からの創造","物書き生活と道具箱"]
tags : ["7wriner"]
draft : false
author : 倉下忠憲
---

前回：<a href="https://rashita.net/blog/?p=23271" target="_blank">情報管理ツール：中ぐらいの断片を扱うためのツール</a>

<h2>7wriner</h2>

現在開発真っ最中の7wriner（セブンライナー）というツールがある。

で、このツール、最初はまったく別の目的で作り始めたのだが、途中から「これって中くらいの断片扱うのに最適じゃね？」ということに気がついた。使っていると、これまでのツールにはなかった感触が得られたのだ（その辺の顛末は、現在<a href="https://rashita.net/blog/?page_id=4556" target="_blank">メルマガ</a>で連載しているのでご興味あれば）。

その7wrinerは、以下のようなUIになっている。

※例１
<a href="https://rashita.net/blog/?attachment_id=23283" rel="attachment wp-att-23283"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-12.png" alt="" width="543" height="745" class="alignnone size-full wp-image-23283" /></a>

※例2
<a href="https://rashita.net/blog/?attachment_id=23284" rel="attachment wp-att-23284"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-13.png" alt="" width="544" height="754" class="alignnone size-full wp-image-23284" /></a>

上の入力欄で入力する。下にカードとして保存される。カードは固定長ではなく、入力した文字サイズに合わせて作成される。アウトライナーのように一行単位でもなく、かといってEvernoteのように大きな余白が生まれることもない。そういうゴルディロックスなサイズ感が7wrinerである。

で、これはほとんどTwitterと同じなのだが、もちろん違いはある。

<ul>
<li>文字数の制限はない</li>
<li>作成したカードは後から編集できる</li>
<li>カードの順番の並び替えができる</li>
</ul>

この辺の操作感は、WorkFlowyやUlyssesに近い。ただし、である。7wrinerは、その名の通り7つしかラインがない。

※画面に表示されるのは３ラインまで。非表示なラインがあと４つある。
<a href="https://rashita.net/blog/?attachment_id=23287" rel="attachment wp-att-23287"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-15.png" alt="" width="1255" height="725" class="alignnone size-full wp-image-23287" /></a>

中央に表示されている一列のカードの並びが「ライン」であり、7wrinerはそれを左右に移動させて使うのだが、そのライン数に上限がある。WorkFlowyやUlyssesのようにいくらでも作成できるわけではない。Twitterは文字数制限だが、7wrinerはライン数制限というわけだ。

もちろんそこにはきちんとしたツール哲学があるわけだが、今回その話は割愛しよう。

<h2>反・大仰さ</h2>

7wrinerは、徹底的に大仰さから距離を置いている。

まず、入力欄の小ささ。このおかげで、気楽に断片を書き込める。入力欄が大きいほど（広いほど）、心理的に大きな文章が要求されるので、ここは大切な要件だ。

また、カードは階層を持たないし、作れない。それぞれのカードはどこかのラインに位置するだけ。以上だ。

複雑な階層どころか二階層すら作れない。単に配置するだけ、ただ置くだけ。それ以上考える必要はないし、<strong>考えることもできない</strong>。

さらにカードは、通常かヘッダーの二種類しかない。カードをダブルクリックすれば通常からヘッダーに変わり、文字が太くなったりボーダーが濃くなるのだが、基本的な違いはそれだけである（もう少し違いはあるが枝葉なので省略する）。

結局、7wrinerでは、カードの扱いや情報構造について複雑に<strong>考えることができないようになっている</strong>。ゆえに、断片を気楽に置いておけるし、気楽にその操作ができる。

<h2>最低限の装飾</h2>

テキストの装飾に関しても、基本的にはプレーンであり、やろうと思えばリンクをぶっ込めるくらいである。

※リンクをコピペした例
<a href="https://rashita.net/blog/?attachment_id=23285" rel="attachment wp-att-23285"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-14.png" alt="" width="545" height="632" class="alignnone size-full wp-image-23285" /></a>

一応画像も扱えるし、太字にもできるし、引用ブロックを挿入することも、コーディング的には可能なのだが、そこにはあまり注力しないようにしている。

そういう機能があってもいいのだが、それはオプションというか奥に隠されているくらいでちょうどいい。

<h2>入力位置の固定</h2>

もう一つ、7wrinerがTwitterに近く、他の情報管理ツールと違うのが、入力位置の固定である。

カードの作成場所は、7wrinerでは固定されている。どれだけラインを移動しても、どれだけカードを並べても、新規カードは同じ場所（位置）から作成される。これがなかなか安定感がある。

この入力位置の固定と、情報構造（≒階層）の欠落が合わさることで、7wrinerを使っているときのユーザーの視座は常に同一である。どこかに「潜るような」ことはないし、「上るような」こともない。言い換えれば、情報構造の中で迷うことがない（だからこそ、ラインは7本までなのだが、やはりそれも割愛しよう）。

一応、全ラインを俯瞰するオーバービューモードというのがあるのだが、これは通常モード(normal mode）に対する特殊なビューであり、WorkFlowyのようなすべての項目を表示するのとは違っている。

※オーバービューモード
<a href="https://rashita.net/blog/?attachment_id=23289" rel="attachment wp-att-23289"><img src="https://rashita.net/blog/wp-content/uploads/2017/11/screenshot-16.png" alt="" width="1425" height="738" class="alignnone size-full wp-image-23289" /></a>

WorkFlowyでは特定の項目にズームすることも、全項目を表示させることも、基本的には等価であるのだが、7wrinerではそうではない。俯瞰は特殊なビュー形態であり、基本は一本のラインの表示である。私たちの意識が、そうであるように、だ。

<h2>next step</h2>

7wrinerでは、ラインを回す操作を通じて、注意のカーソルをクルクルと回す。

そこには、上位もなければセントラルもない。暫定的な、便宜的な、カレントなラインが一つあるだけである。

7wrinerは、ツリー構造でもディレクトリ構造でもない。むしろ、問おう。なぜ私たちの注意（意識と言ってもいい）や情報を扱うツールが、ツリー構造でなければならないのか、と。本当にそれは適切な形なのか、と。