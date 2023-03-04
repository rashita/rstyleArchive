---
title : Scrapboxで、特定ページ内の記述をアラートする
link : 24894
date : Fri, 08 Jun 2018 02:26:05 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

最近、私の作業用Scrapboxプロジェクトでは、最初にページを読み込むとアラートが表示されるようになっています。

<a href="https://rashita.net/blog/?attachment_id=24895" rel="attachment wp-att-24895"><img src="https://rashita.net/blog/wp-content/uploads/2018/06/screenshot.png" alt="" width="1329" height="572" class="alignnone size-full wp-image-24895" /></a>

で、この中身は、以下のようなページから取得しています。

<a href="https://rashita.net/blog/?attachment_id=24896" rel="attachment wp-att-24896"><img src="https://rashita.net/blog/wp-content/uploads/2018/06/screenshot-1.png" alt="" width="950" height="576" class="alignnone size-full wp-image-24896" /></a>

このページのコードブロック（灰色の部分）を書き換えれば、アラートに表示される内容も変わる、という仕組みです。これで、明日以降の自分に対して能動的に情報を「先送り」できます。

UserScriptは以下に。

<a href="https://scrapbox.io/scrapboxlab/%E7%89%B9%E5%AE%9A%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%8B%E3%82%89%E6%83%85%E5%A0%B1%E3%82%92%E8%AA%AD%E3%81%BF%E8%BE%BC%E3%82%93%E3%81%A7%E3%82%A2%E3%83%A9%E3%83%BC%E3%83%88%E3%81%99%E3%82%8B">特定ページから情報を読み込んでアラートする - Scrapbox研究会</a>

で、まずこれって他にもいろいろアレンジできます。覚えたい英単語を一日ひとつ表示させるとか、書籍からの書き抜きを一つ表示させるとか、そういうこともできそうです。

もちろん、そういうのはしょぼいと言えばしょぼいわけですが、自分が蓄積したデータを「使っている」ことは間違いありません。で、このような使い方って、既存の情報整理ツールだとなかなか敷居が高かったわけです。

EvernoteかつMacならば[<a href="https://scrapbox.io/rashitamemo/AppleScript">AppleScript</a>]がありますが、それ以外の環境ならAPIを叩く必要があり、でもってそのためのハードルは艱難辛苦です（あるいはそのように感じられます）。WorkFlowyにはそもそもAPIがありません。

その点Scrapboxは、ページデータの取得くらいなら簡単にできます。クロスドメインの処理は私にはさっぱりですが、少なくともScrapbox内であれば、上記のようなことが、私の様な[<a href="https://scrapbox.io/rashitamemo/%E6%97%A5%E6%9B%9C%E5%A4%A7%E5%B7%A5%E3%83%97%E3%83%AD%E3%82%B0%E3%83%A9%E3%83%9E%E3%83%BC">日曜大工プログラマー</a>]にもできてしまうのです。

一般的な情報整理ツールにおいて、情報を「使う」とは、参照し想起することが強くイメージされていましたが、Scrapboxに関しては上記のような利用方法もあります。

これは結構すごいことではないか、といろいろな情報整理ツールを使っていても感じるわけです。