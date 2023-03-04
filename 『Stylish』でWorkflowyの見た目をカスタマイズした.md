---
title : 『Stylish』でWorkflowyの見た目をカスタマイズした
link : 15453
date : Wed, 11 Feb 2015 03:13:35 +0000
categories : ["0-知的生産の技術","アウトライナーで遊ぼう"]
tags : ["stylish","workflowy","アウトライナー","考具"]
draft : false
author : 倉下忠憲
---

あ〜、なるほどね〜、ぐらいに思いました。最初は。

<a href="http://mmkns.tumblr.com/post/110594873857/chrome-stylish-web" target="_blank">Chrome拡張『Stylish』でWEBアプリを自分のモノにする</a>（mmkns）

<blockquote>『Stylish』はFirefoxやOperaにもある人気の拡張機能で、これを使えば「ユーザースタイルを管理するツールで、ウェブのスタイルを変更」(<a href="https://chrome.google.com/webstore/detail/stylish/fjnbnpbmkenffdnngjfgmeleoegfcffe?hl=ja">公式</a>より)できます。

（中略）

Stylishの存在は以前から知ってましたが、別にデフォルトでいいじゃんと思って使ってなかったんですよね。</blockquote>

私も、「デフォルトのスタイルで困ってないし、別に使わなくてもいいかな」と思いましたよ。でも、Firefoxにもあることだし、とりあえず試してみようか、と思ったわけです。とりあえずMind。

で、以前からUIが使用感に与える影響について検討していたつもりでしたが、これがまあ全然わかっていなかったですね。

<H3>違うツール</H3>

簡単に言うと、こういうのが、

<a href="https://rashita.net/blog/wp-content/uploads/2015/02/screenshot1.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/02/screenshot1-1024x597.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-15454" /></a>

こうなります。

<a href="https://rashita.net/blog/wp-content/uploads/2015/02/screenshot2.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/02/screenshot2-1024x585.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-15455" /></a>

別物、と言って差し支えないでしょう。

もちろん、アウトライナー的機能という点でみれば同じツールです。機能原理主義者にしてみれば何も変わっていないに等しいでしょう。でも、一日に長い時間触れるツールであるならば、見た目の要素ってかなり大きいです。はい。

<H3>施した変更点</H3>

ちなみに、『Stylish』はCSSをブラウザ側で上書きするという感じなのですが、一から自分でCSSを書く必要はありません。

「このサイト用のスタイルを探す」で、誰かが書いたCSSを拝借することができます。Workflowyにもいくつかありました。

さらに、そのCSSを書き換えることもできるので、カスタマイズも容易です。

※ブラウザから直接CSSを書き換えられます。
<a href="https://rashita.net/blog/wp-content/uploads/2015/02/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/02/screenshot3.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15460" /></a>

私は「workflowy.com - clean and bright」をベースにカスタマイズしてみました。手を加えた箇所は

<ul>
<li>背景色をベージュに</li>
<li>ページの上・左マージンを詰める</li>
<li>トップの見出し項目を太字に</li>
<li>フォントを変更</li>
<li>フォントサイズを小さく</li>
</ul>

あたりです。

一応CSSもちらりと。

<H4>背景色をベージュに</H4>

<code>.page {
background: #FFFEEC !important;
}</code>

<H4>ページの上・左マージンを詰める</H4>

<code>.page {
  margin:0 !important;
  padding:10px 150px 20px;
  width:100%;
  max-width:100%;
  box-sizing:border-box
}</code>

<H4>トップの見出し項目を太字に</H4>

<code>div.project.selected > div.children > div > div.name div.content {
  font-weight: bold !important;
}</code>

<H4>フォントを変更</H4>

<code>#documentView {
    font-family: Sana, Calibri, Trebuchet, Verdana, sans-serif;
}</code>

<H4>フォントサイズを小さく</H4>

<code>.selected .project > .name > .content, .nameEditor > textarea {
  font-size: 13px !important;
  color: #191919 !important;
  font-weight: normal !important;
}</code>

<H3>さいごに</H3>

CSSの小難しいことがわからなくても、とりあえず何かスタイルをあててみて、そのコードをちょこちょこ書き換えてWorkflowyでどう表示が変わるのかを確認していくと、何と何が対応しているのかぐらいは推測がつくかと思います。

一応書いておくと、pxと書いてあるものは何かの大きさ。#191919 のように、#の次に0〜9、あるいはa~fまでの文字が６つ（ないし３つ）続いているのは何かの色です。rgba()も色。あとは、それぞれの文をそのままググれば、だいたいわかると思います。

ただ、あまりデザインに凝り出すと時間が無限回廊に吸い込まれてしまうので注意してください。

では、Let's make your List!


→関連する記事：<a href="https://rashita.net/blog/?p=15464" target="_blank">Workflowyでnoteを全文表示にしてみた</a>