---
title : Workflowyでnoteを全文表示にしてみた
link : 15464
date : Thu, 12 Feb 2015 03:42:22 +0000
categories : ["0-知的生産の技術","アウトライナーで遊ぼう"]
tags : ["stylish","workflowy","アウトライナー","考具"]
draft : false
author : 倉下忠憲
---

先日の記事で、Stylishを用いたWorkflowyのカスタマイズを紹介しました。

<a href="https://rashita.net/blog/?p=15453" target="_blank">『Stylish』でWorkflowyの見た目をカスタマイズした</a>

<blockquote>もちろん、アウトライナー的機能という点でみれば同じツールです。機能原理主義者にしてみれば何も変わっていないに等しいでしょう。</blockquote>

これ嘘でした。はい、すいません。

カスタマイズによって、アウトライナー的機能も変えられます。

<H3>ノートの全文表示</H3>

変えられるのは「note」の部分です。それぞれの項目に付けられる「メモ」のようなものですね。キーボード・ショートカットならshift+enterで入力できます。

通常のWorkflowyでは、このnoteは（入力時以外は）冒頭の一行しか表示されません。まあ、メモですからね。それで良いでしょう。でも、その表示スタイルをStylishでハックすることも可能です。

ちょっと、比較動画を作ってみました。

<iframe width="420" height="315" src="https://www.youtube.com/embed/di5YAWgC5vk" frameborder="0" allowfullscreen></iframe>

前半はCSSに手を加えていないバージョン。項目を選択したときだけnoteが全文表示されています。動画の後半はCSSハック後で、noteの全文が表示されるようになっています。

さすがにこれを「同じ機能」と呼ぶのは無理がありそうです。

私はこれまで「一行だけ表示」が気に入らなくて、Workflowyのnoteはほとんど使っていませんでした。しかし、全文表示ができるとなると話は変わります。これまで使ってこなかった、「文章入力」の場面（ようするにエディタ的使い方）で力を発揮してくれるかもしれません。

<H3>さいごに</H3>

ちなみに、Stylishで見つけられるテーマで「full note」と書いてあれば、全文表示になっています。

自分でカスタマイズする場合は、

<code>DIV.notes DIV.content {
  height: auto !important;
  overflow: visible !important;
}</code>

を書き加えると良いでしょう。逆に、full noteなテーマで一行表示に戻したい場合は、上記に似た記述の部分を削除すると戻せるはずです。

ではでは、楽しいアウトラインライフを。
