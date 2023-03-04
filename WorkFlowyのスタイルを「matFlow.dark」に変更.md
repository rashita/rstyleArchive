---
title : WorkFlowyのスタイルを「matFlow.dark」に変更
link : 16896
date : Mon, 12 Oct 2015 03:23:27 +0000
categories : ["アウトライナーで遊ぼう","物書き生活と道具箱"]
tags : ["stylish","workflowy"]
draft : false
author : 倉下忠憲
---

WorkFlowyのメインのスタイル（※）を変更しました。新しく使い始めたのは「matFlow.dark」です。
※stylishのテーマのことです。

こんな感じになります。

<a href="https://rashita.net/blog/?attachment_id=16897" rel="attachment wp-att-16897"><img src="https://rashita.net/blog/wp-content/uploads/2015/10/screenshot3-500x279.png" alt="screenshot" width="500" height="279" class="alignnone size-medium wp-image-16897" /></a>

ちなみに、テーマを外すとこう。

<a href="https://rashita.net/blog/?attachment_id=16898" rel="attachment wp-att-16898"><img src="https://rashita.net/blog/wp-content/uploads/2015/10/screenshot4-500x279.png" alt="screenshot" width="500" height="279" class="alignnone size-medium wp-image-16898" /></a>

まったく別ツールですね。

<H3>特徴</H3>

このテーマの面白いところは、どこかのトピックにZoom inすると、

<a href="https://rashita.net/blog/?attachment_id=16899" rel="attachment wp-att-16899"><img src="https://rashita.net/blog/wp-content/uploads/2015/10/screenshot5-500x434.png" alt="screenshot" width="500" height="434" class="alignnone size-medium wp-image-16899" /></a>

このように見出しがヘッダーっぽくスタイルされているところです。なんかちょっとかっこいいですよね。

<a href="https://rashita.net/blog/?attachment_id=16900" rel="attachment wp-att-16900"><img src="https://rashita.net/blog/wp-content/uploads/2015/10/screenshot6-500x161.png" alt="screenshot" width="500" height="161" class="alignnone size-medium wp-image-16900" /></a>

あと、トピックを閉じたものと比較してもらうとわかりますが、開いているとダッシュ線のボーダーが出てきて、閉じているとそれが消えます。なかなか興味深い仕様です。

もう一つ、見出しにあたるトピックのノートは、背景色が変わります。

<a href="https://rashita.net/blog/?attachment_id=16901" rel="attachment wp-att-16901"><img src="https://rashita.net/blog/wp-content/uploads/2015/10/screenshot7-500x197.png" alt="screenshot" width="500" height="197" class="alignnone size-medium wp-image-16901" /></a>

そのノートがどこに従属しているのかが、視覚的にずいぶんわかりやすくなりますね。なんとなくですが、ちょっとカードをイメージしました。

<H3>カスタマイズ</H3>

ちなみに、使う上で、少しばかりスタイルに手を入れています。

一つは、Zoom inしていない状態のノートも背景色を変えるようにしたこと。少しだけ薄めの灰色になっています。ノートをあまり使わない人は気にならないでしょうが、案外「これはノートなのかどうか」というのが通常のスタイルだとわかりにくかったりするんですよね。背景色を変えておけばばっちりです。

<a href="https://rashita.net/blog/?attachment_id=16902" rel="attachment wp-att-16902"><img src="https://rashita.net/blog/wp-content/uploads/2015/10/screenshot8-500x71.png" alt="screenshot" width="500" height="71" class="alignnone size-medium wp-image-16902" /></a>

あと、「matFlow.dark」のノーマル状態では、ノートの改行が改行として表示されず常に詰められてしまうので、それを改行表示アリに変えておきました。

<code>.noted > .notes > .content {
    height: auto !important;
    min-height: 20px !important;
    overflow: visible !important;
    line-height: 20px !important;
    display: block !important;
    -webkit-box-orient: inherit !important;
    -webkit-line-clamp: inherit !important;
    white-space: pre !important;
}
</code>

の、「white-space: pre !important;」がその指定です。元に戻したければ、preを「inherit」にすればOK。

<H3>さいごに</H3>

これまで私は「エディタの背景色と言えばベージュでしょ」と、黒系の背景色は使ったことがなかったんですが、なかなか良い感じです。目に優しいとかではなく、心のモードが切り替わる効果があり……そうな気がします。それは言うならば、俺は今アウトライナーを使っているんだぞ、というような気持ちのスイッチが入るといった感じです。

というわけで、しばらくこのスタイルでいくことにしました。細かいカスタマイズがあれば、また書いてみます。

<strong>▼その他リンク：</strong>
<a href="https://rashita.net/blog/?p=15453">R-style » 『Stylish』でWorkflowyの見た目をカスタマイズした</a>
<a href="http://cyblog.jp/modules/weblogs/18812">WorkFlowyでハイライトを使えるようにカスタマイズする方法 | シゴタノ！</a>