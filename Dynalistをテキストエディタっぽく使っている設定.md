---
title : Dynalistをテキストエディタっぽく使っている設定
link : 29161
date : Tue, 16 Jul 2019 02:48:11 +0000
categories : ["アウトライナーで遊ぼう"]
tags : ["css","dynalist","stylus","アウトライナー"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=29152">前回の記事</a>で、テキストエディタっぽくDynalistを使っていると紹介した。

今回はその設定を見ていこう。

<h2>テーマとCSS</h2>

まず標準状態。テーマは「Sepia」を選択している。

<a href="https://rashita.net/blog/?attachment_id=29162" rel="attachment wp-att-29162"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-9-700x521.png" alt="" width="700" height="521" class="alignnone size-large wp-image-29162" /></a>

ここで「LAYOUT」を「List」から「Article」に変更する。

<a href="https://rashita.net/blog/?attachment_id=29163" rel="attachment wp-att-29163"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-10.png" alt="" width="440" height="373" class="alignnone size-full wp-image-29163" /></a>

<a href="https://rashita.net/blog/?attachment_id=29164" rel="attachment wp-att-29164"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-11-700x511.png" alt="" width="700" height="511" class="alignnone size-large wp-image-29164" /></a>

これで行頭のバレットが取れた。が、このままだと行間が広すぎる。そこでブラウザ拡張の「Stylus」を使ってCSSを上書きする。

<code>
.is-compactDensity.is-article-view .Node-self, .is-cozyDensity.is-article-view .Node-self, .is-comfortableDensity.is-article-view .Node-self {
    padding-top: 0px;
    padding-bottom: 0px;
}
</code>

こうすれば行間が縮まる。

さらに右上に常時表示されている検索ボタンとview optionボタンが邪魔なので、ホバーしたときだけ表示するようにする。

<code>
.DocumentTools-overlay:not(:hover){
    opacity:0;
}
.DocumentTools-icon:not(:hover){
        opacity:0; 
}
</code>

<a href="https://rashita.net/blog/?attachment_id=29167" rel="attachment wp-att-29167"><img src="https://rashita.net/blog/wp-content/uploads/2019/07/screenshot-12-700x549.png" alt="" width="700" height="549" class="alignnone size-large wp-image-29167" /></a>

これで邪魔なものはほとんど消えた。いかにもテキストエディタっぽくなる。ちなみに、大きい画面の方の背景色は以下で変更してある。

<code>
.DocumentContainer, .AppContainer.is-borderShowing.is-globalSearch .DocumentContainer {
    background: whitesmoke ;
    background-image: none;
}
</code>

この辺はお好みで。

<h2>表示に加えて</h2>

上記のような設定をすれば、アウトライナーを使っている気分なく、アウトライナーを使うことができる。特にDynalistはいろいろなことができる分、表示されるものも多いので、文章を書く段階ではわりと視覚的重さが発動されてしまう。だからこその、要素の隠蔽だ。

ただし、こう設定しても、項目をホバーしたときに表示されるメニューボタンとズームボタンはいかんともしがたい。これがまた、気になるのである。

なので、解決策は、ホバーさせないこと、つまりマウス操作を極力避けることである。項目の移動やズームに関してはショートカットで操作できる。別の項目に移動させる(move to）もショートカットがある。だから、ある程度操作を覚えてしまえば、マウスを触らなくてもたいていのことはできる。つまり、左側のアイコンを見なくても済む。素晴らしい。

ショートカットの簡単なまとめは以下の記事に書いてあるので、参考にする場合はどうぞ。

<a href="https://rashita.net/blog/?p=28274">Dynalistでよく使うショートカットキー – R-style</a>


<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer"><img src="https://images-fe.ssl-images-amazon.com/images/I/51HoJpXhvnL._SL160_.jpg" alt="アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank" rel="noopener noreferrer">amazlet</a> at 19.07.16</div></div><div class="amazlet-detail">技術評論社 (2016-07-09)<br />売り上げランキング: 134,782<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank" rel="noopener noreferrer">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

