---
title : Scrivenerへの散歩道#011　ページを制御する
link : 14255
date : Sat, 06 Sep 2014 02:32:34 +0000
categories : ["scrivenerへの散歩道"]
tags : []
draft : false
author : 倉下忠憲
---

PDFやEPUBには、「ページ」という概念があります。

1ページ目、2ページ目、3ページ目、……

というやつですね。

今回は、Scrivenerでの「ページ」を扱い方を紹介します。

<span class="appIcon"><img class="appIconImg" height="60" src="http://a4.mzstatic.com/us/r30/Purple4/v4/59/f5/79/59f57985-7c59-0b0c-48ba-cf8fc7bfd9e5/Scrivener.60x60-50.png" style="float:left;margin: 0px 15px 15px 5px;"></span><span class="appName"><strong><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store">Scrivener</a></strong></span><br><span class="appCategory">カテゴリ: 仕事効率化, 教育</span><br><span class="badgeS" style="display:inline-block; margin:6px"><a href="https://itunes.apple.com/jp/app/scrivener/id418889511?mt=12&uo=4&at=11l4y8" target="itunes_store" style="display:inline-block;overflow:hidden;background:url(http://linkmaker.itunes.apple.com/htmlResources/assets//images/web/linkmaker/badge_macappstore-sm.png) no-repeat;width:81px;height:15px;"></a></span><br style="clear:both;">

<H3>ページ状態のビュー</H3>

まずは「ページビュー」から。

たとえば、以下のようなファイルがあったとしましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot4.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot4.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14256" /></a>

ごく普通の表示状態です。ここでメニューの「View」から「Page View」→「Show Page View」を選択してみます（※）。
※shift + option + command + P でも可

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot5.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot5.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14257" /></a>

このような表示状態に変化しました。これがページビューです。PDFファイルだと、こんな感じに見えるよ、というのがページビューの役割。最終的なコンパイル先がPDFなら、常にこの状態で入力しても良いかもしれません。

<H3>改ページを挿入</H3>

という点を踏まえた上で、改ページの説明に入ります。

通常の状態では、連続したテキストはずっと続きます。以下のように、テキストとテキストの境目でも、ページは変わっていません。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot6.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14258" /></a>

しかし、演出的観点から「ここでページを変えたい」と思う場合もあるでしょう。そういうときは、メニューの「Edit」から「insert」→「Page Break」です。

※改ページしたい！
<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot7.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14259" /></a>

※改ページされた！
<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot8.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14260" /></a>

このように改ページが入りました。ちなみに、この改ページは「特殊な改行」ぐらいに認識しておけばOKで、その改行をdeleteすれば、改ページも消えます。

<H3>コンパイル時に自動的に改ページを挿入</H3>

構成として、必ず改ページを入れたい部分があるかもしれません。たとえば、章と章の変わり目などです。それら全てにいちいち改ページを挿入していくのは、あまり効率的とは言えません。

そこはコンパイルで対応しましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot9.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14261" /></a>

コンパイルのオプション設定の「Contents」タブにある「Pg Break Before」にチェックを入れれば、そのファイル（あるいはフォルダ）の前に改ページが入ります。全部にチェックを入れたければ、option+クリック、すればOKです。

※こうなる
<a href="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot10.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/09/screenshot10.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14262" /></a>

<H3>さいごに</H3>

以上が基本的なScrivenerのページの取り扱いになります。

次回は、でんでんコンバーターを使った改ページの制御法について書いてみます。