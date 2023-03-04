---
title : iOSのショートカットを学ぶ９
link : 28639
date : Tue, 18 Jun 2019 22:00:52 +0000
categories : ["プログラミング"]
tags : ["evernote","ios","iosショートカット"]
draft : false
author : 倉下忠憲
---

前回：<a href="https://rashita.net/blog/?p=28628">iOSのショートカットを学ぶ８</a>

前回は、「FastEverもどき」のアレンジバージョンをいろいろ考えてみた。今回は、別のアプローチにチャレンジしてみよう。

やりたいのは、特定のノートへの追記である。具体的に言えば、今日の日付をタイトルに持つノートへ次々と追記していく。そういう日記的な運用ができるショートカットを作ってみたい。

<h2>「メモに追加」</h2>

必要なものは、二つある。一つは特定のノートに追記するアクション、もう一つは今日の日付を取得するアクションだ。

まずは前者だが、これは簡単である。検索ボックスに「Evernote」と入れれば、それらしいのが見つかる。

<a href="https://rashita.net/blog/?attachment_id=28320" rel="attachment wp-att-28320"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/1D5BEC24-B03E-4E70-ABBD-DADC929B2980.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28320" /></a>

「メモに追加」が今回の用途にぴったりだろう。

<a href="https://rashita.net/blog/?attachment_id=28641" rel="attachment wp-att-28641"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/DF60B0F7-BA48-4F7D-8448-64B3A3CC2B26.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28641" /></a>

この「ノートタイトル」部分に今日の日付を入れると、Evernoteが検索してくれて、見つかったノートに内容を追記してくれる、という寸法である。追記の中身は「入力を要求」でいいだろう。

<a href="https://rashita.net/blog/?attachment_id=28642" rel="attachment wp-att-28642"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/8B2F9045-5258-417E-9CCA-62750E158433.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28642" /></a>

<h2>日付</h2>

問題は今日の日付である。さすがに手で入力するのは避けたい。そこで検索ボックスに「日付」と入れてみる。

<a href="https://rashita.net/blog/?attachment_id=28643" rel="attachment wp-att-28643"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/3326DC83-56EE-4697-8424-D3450B5388EA.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28643" /></a>

いくつかあるが「日時」というのがそれっぽいので設置してみる。

<a href="https://rashita.net/blog/?attachment_id=28644" rel="attachment wp-att-28644"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/390F6B41-C299-46C2-AE97-EAC281CA22B0.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28644" /></a>
「現在の日付」とあるので目的のものだろう。

ただしこのままだと、時間なども含まれてしまう。

<a href="https://rashita.net/blog/?attachment_id=28645" rel="attachment wp-att-28645"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/DD3315A4-2345-419F-9821-EBABEE71BD56.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28645" /></a>

これを変えたい。そこで「日付をフォーマット」である。

<a href="https://rashita.net/blog/?attachment_id=28646" rel="attachment wp-att-28646"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/07E78E43-D2C0-4348-A789-72D890F06943.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28646" /></a>

この日付フォーマットを「カスタム」にする。

<a href="https://rashita.net/blog/?attachment_id=28647" rel="attachment wp-att-28647"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/753302AA-70C4-4F92-BF77-1AE8CD907197.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28647" /></a>

<a href="https://rashita.net/blog/?attachment_id=28648" rel="attachment wp-att-28648"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/A8F9DC67-4139-4237-BD04-1D536F20054B.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28648" /></a>

私は月と日付が欲しいので「文字列をフォーマット」の中身を以下のようにしてみた。年が必要ならyyyyを追加すればいいだろう。

<a href="https://rashita.net/blog/?attachment_id=28649" rel="attachment wp-att-28649"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/74980801-3585-4B98-8CD7-B6326FB1BC5A.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28649" /></a>

あとはこれを組み合わせればいい。以下のような流れになった。

<a href="https://rashita.net/blog/?attachment_id=28651" rel="attachment wp-att-28651"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/685AD05B-4C3B-4F83-9140-1749BAD6C51E.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28651" /></a>

<a href="https://rashita.net/blog/?attachment_id=28650" rel="attachment wp-att-28650"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/FB22EF06-3329-403D-B934-24BFCE094286.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28650" /></a>

<h2>テスト</h2>

では、実際にやってみよう。

<a href="https://rashita.net/blog/?attachment_id=28652" rel="attachment wp-att-28652"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/B0E91EE0-63F8-4369-B010-0346A3B752FB.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28652" /></a>

<a href="https://rashita.net/blog/?attachment_id=28653" rel="attachment wp-att-28653"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/screenshot-6.png" alt="" width="518" height="521" class="alignnone size-large wp-image-28653" /></a>

無事、「6月18日」のノートに内容が追記されている。

これで、このショートカットを起動するたびに、「&#x1f4c5;6月18日(火)」に追記されていき、日付が変わったら「&#x1f4c5;6月19日(水)」のノートに追記される、というショートカットができた。もちろん、ノートの中身については、前回書いたようなアレンジバージョンがいくらでも作れることは言うまでもない。

<h2>さいごに</h2>

というわけで、今回はPostEver（あるいはDayEntry）のような振る舞いをするショートカットを作ってみた。ちなみに、ノートを検索してから追記するので、動作自体は実にもっさりしていることだけはお断りしておこう。快適な動作が必要な場合は、やはりアプリを使うのが良い、というのは致し方のない結論である。

さて、次回はとりあえずの最終回となる。全体のまとめなどを書ければいいが、何か別のアレンジについて書くかもしれない。

