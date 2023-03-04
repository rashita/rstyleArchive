---
title : Evernoteのデイリータスクリストを業務日誌にできないか
link : 18447
date : Thu, 30 Jun 2016 04:19:00 +0000
categories : ["evernoteの使い方"]
tags : ["evernote","業務日誌"]
draft : false
author : 倉下忠憲
---

<a href="http://lala.idea4u.net/archives/108439444#PpYQQYB.twitter_tweet_count_m">【レビュー】現在のデジタル日記の書き方 | 知的生活ネットワーク</a>

<blockquote>
1988年からデジタル日記を書き始めて27年ほどになります。

前回2013年に，当時の日記の書き方をレビューしていましたが，それから3年たち書き方もかわっているので，現時点での日記の書き方についてまとめておこうと思います。
</blockquote>

実に楽しそうです。

なんとなく、自分の場合は、「記録を残していけば、勝手に日誌（日記）になる」のが理想だと思っていましたし、実際理想ではあるのですが、上の記事では毎日10分ほどの時間を使って整理・整形が行われているようです。後から見返す、ということを念頭においた場合、そういう作業も必要なのでしょう。

ともかく記録だけは先にしておいて、それらを後から集めて、見やすいように修正しておく。

今までの自分には欠けていた視点でした。

じゃあ、それを自分に応用したらどうなるのか。

実に楽しそうです。

<h3>改定案</h3>

私は、一日ごとのタスクを管理する「デイリータスクリスト」用のノートを作成しています。ここで扱われるデータも、もちろん業務日誌の範囲でしょう。

<a href="https://rashita.net/blog/?attachment_id=18448" rel="attachment wp-att-18448"><img src="https://rashita.net/blog/wp-content/uploads/2016/06/screenshot20-500x538.png" alt="screenshot" width="500" height="538" class="alignnone size-medium wp-image-18448" /></a>

しかし、これだけでは情報量は不足しています。その日の行動を想起できるほどではありません。だったらどうするか。上記のアイデアを応用するなら、後からつけ加えればよいのです。

何を？

たとえば最近MemoFlowyのアップデートで使いやすくなったWorkFlowyに行動履歴を貯めておき、それをコピペする？　いや、その場合タイムスタンプがないじゃないか。でも、自分で入力すればどうか。いやいやいや、Evernoteだったら初めからタイムスタンプ付きだぜ。それにinboxだってEvernoteなんだから。

ふと、ある記事を思い出しました。

<a href="http://cyblog.jp/modules/weblogs/21257">「１年前の今日のこの時間は何をしていたのか？」を知ると、次の一歩が見えてくる | シゴタノ！</a>

この記事では「一年前の自分を振り返る方法」が紹介されています。この「一年」をXに置き換えてみましょう。「X前の自分を振り返る」。そして、Xに一日を代入します。「一日前の自分を振り返る方法」。

これって、冒頭に紹介した記事の「デジタル日記のフロー」に近いんじゃないか。

一日前のノートを表示する方法は、関連で紹介されている以下の記事ですぐに分かりました。

<a href="http://cyblog.jp/modules/weblogs/journal/15440">Evernoteの検索で特定の日以降に作成されたノートのみを表示させる方法 | じゃーなる</a>

検索構文：「created:day-1」

これで昨日（と今日）作成したノートが閲覧できます。もちろん、こんな検索を使わなくても「すべてのノート」を表示して、少しスクロールさせれば昨日分はすぐに発見できます。でも、検索を使うことにはちゃんと意味があるのです。

とりあえず、そうして絞り込んだノートをどげんかしなければなりません。もちろん、ノートリンクです。昨日作成したノートすべてのノートリンクを取得し、それをその日のデイリータスクリストノートにぺたっと。

<a href="https://rashita.net/blog/?attachment_id=18449" rel="attachment wp-att-18449"><img src="https://rashita.net/blog/wp-content/uploads/2016/06/screenshot21-500x428.png" alt="screenshot" width="500" height="428" class="alignnone size-medium wp-image-18449" /></a>

これで一日の情報量が増しました。これをちらっと見るだけで、その日ブログやメルマガで何を書いたのか、どんなアイデアを書き留めたのかが一望できます。クリップしたWebページも明らかですね。

おぉ、完璧じゃん。

あとは上記の検索を保存し（※）、「昨日のノート」とでも名前をつければばっちり。それをショートカットに置いておけば、「そうそう、昨日のノートをチェックしておかないとな」と自分にリマインドできます。これが習慣化への鍵となるわけです。
※<a href="https://help.evernote.com/hc/ja/articles/209005267">「保存された検索」を作成する方法 – Evernote ヘルプ＆参考情報</a>参照のこと。

いや、まてよ。

「昨日作成されたノート」でいいのだろうか。これを「昨日更新されたノート」にしたらどうなるんだろうか。

<a href="https://dev.evernote.com/intl/jp/doc/articles/search_grammar.php">検索構文 - Evernote Developers</a>

上記ページをみてみると、「created」ではなく、「updated」とすれば、更新したノートにアクセスできます。

考えてみると、ノートは作成するだけではなく、作成したノートに追記することもあります。アイデアノートなどが特にそうですが、プロジェクト情報を扱うノートも同様です。「created」では、そうしたノートへの追記が追跡できません。となると、「updated」の方がよいでしょう。

<h3>さいごに</h3>

こうして、「Evernoteで業務日誌管理フロー ver.α」が完成しました。まだまだ改善の余地はありますが、少なくとも、これまでより「デイリータスクリスト」ノートが情報的彩りを増していることは確かです。

作業自体は単調なので、スクリプトによる自動化も検討課題ですが、まずは手作業でコツコツ進めて感触を確認していくところからでしょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.06.30</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 4,597<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


