---
title : 直接Postachにクイック投稿できるMacアプリ「goPost」
link : 11535
date : Sat, 28 Sep 2013 07:12:16 +0000
categories : ["物書き生活と道具箱"]
tags : ["applescript","evernote","postach"]
draft : false
author : 倉下忠憲
---

みなさん、Postach使ってますか？

<a href="https://rashita.net/blog/?p=11231" target="_blank">Evernoteをアウトプットツールへと変身させる「Postach.io」</a>

私は以下のサイトで運営しています。

<a href="http://rashita.postach.io/" target="_blank">R-in </a>

公式ページはこちら。

<a href="http://postach.io/" target="_blank">Postach.io</a>

で、このPostachへの投稿なんですが、たとえばiPhoneアプリからだと簡単です。ノートブックやタグを指定できるアプリがたっぷりありますので。

しかし、それと同じ感覚でMacでの投稿はできません。Macのクイックノートは「規定のノートブック」＋「タグなし」になっているので。
※postach用のノートブックを「規定のノートブック」にする荒技もあります。が、その場合でもタグはどうしようもありません。

というわけで、専用のスクリプトを書いてみました。

<H3></H3>
<script src="https://gist.github.com/rashita/5152d285ea5ff4b304f9.js"></script>
<H3></H3>ちょこっとアレンジすれば、publishedだけではくtweetタグなんかも自動的に付けられます。

とりあえず標準のものでよければ、以下からダウンロードできます。

<a href="https://dl.dropboxusercontent.com/u/554861/goPost.zip">goPost.zip</a>

一応最新のMacでの動作確認は済ませておりますが、その他の環境はまったくわかりませんので、あしからず。