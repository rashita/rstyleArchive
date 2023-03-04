---
title : Scrapboxですぐページを作りたい
link : 24814
date : Mon, 28 May 2018 01:20:36 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

<strong>/newページをブックマークしておく。</strong>

プロジェクトを開く→＋ボタンを押す、という手順がまどろっこしく感じる場合は便利。

<h2>解説</h2>

Scrapboxでは、https://scrapbox.io/hogeproject/new が新規作成のページとなる。よって、ここにダイレクトにアクセスすれば、即座に新規のページが作成される。

<a href="https://rashita.net/blog/?attachment_id=24815" rel="attachment wp-att-24815"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-20.png" alt="" width="478" height="295" class="alignnone size-full wp-image-24815" /></a>

<a href="https://rashita.net/blog/?attachment_id=24816" rel="attachment wp-att-24816"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-21.png" alt="" width="1263" height="698" class="alignnone size-full wp-image-24816" /></a>

<h2>応用</h2>

Macのターミナルからopenしてもいい。

<a href="https://rashita.net/blog/?attachment_id=24817" rel="attachment wp-att-24817"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-22.png" alt="" width="382" height="77" class="alignnone size-full wp-image-24817" /></a>

AppleScriptなら <code>do shell script "open https://scrapbox.io/hogeproject/new"</code> でもいいし、あるいはブラウザに直接URLを与えてもいい。それをアプリ化して、HOTキーを設定すれば、キー一発で作成画面に移動できる。

<h2>応用その２</h2>

空っぽではなく、タイトルなどを指定することもできる。たとえば、以下。

<a href="https://scrapbox.io/masui/Scrapbox%E3%81%A7%E6%B0%97%E8%BB%BD%E3%81%AB%E3%83%A1%E3%83%A2%E3%82%92%E3%81%A8%E3%82%8B">Scrapboxで気軽にメモをとる - 増井俊之</a>

これを応用すれば、一発で「その日のノート」を開くことができる。まだそのノートが存在しない場合は新規作成できる。

単に開くだけでなく、本文を付け加えることもできる。

<a href="https://scrapbox.io/help-jp/%E3%83%9A%E3%83%BC%E3%82%B8%E3%82%92%E4%BD%9C%E3%82%8B#58ae7c9a97c29100005b886b">ページを作る - Scrapbox ヘルプ</a>

<code>https://scrapbox.io/hogeproject/ページタイトル?body=本文</code>
※本文にはURLエンコードが必要

たとえば、AppleScriptなどでダイアログを表示させ、そこにメモの内容を入力したら、Scrapboxのその日のノートに書き込む、ということができる。

上の書き方をすると、すでにページが存在する場合は、本文は追記される形になるので、既存のページのことは考えなくて済むのが良い。このスクリプトはちょっと書いてみたいと思う。

<h2>まとめ</h2>

頻繁にページを新規作成する場合は、/newページを活用すること。

<code>https://scrapbox.io/hogeproject/ページタイトル?body=本文</code> も便利だが、本文のURLエンコードを忘れずに。
