---
title : Scrivenerにテキストファイルを分割してインポートする機能。そしてEvernoteからScrivenerへ。
link : 13922
date : Mon, 28 Jul 2014 02:52:22 +0000
categories : ["scrivenerへの散歩道"]
tags : ["applescript","evernote","scrivener"]
draft : false
author : 倉下忠憲
---

Scrivenerにはファイルを取り込む機能がいくつかあるのですが、中でも覚えておきたいものがあります。

それが、「Import and Split」。

テキストファイルを取り込む際、ファイル分割を同時に実行してくれます。

普通は、一枚の大きなテキストファイルを取り込み、その後自分で「Split with Selection as Title」を複数回実行して、ファイルを分割していき、順番の入れ換えといった構成作業を行いやすくするのですが、事前に分割する箇所がわかっているなら、テキストに小細工をすることで、あらかじめ分割された状態でファイルをインポートできます。

実際にみてみましょう。

<H3>ファイルを分割して取り込む</H3>

こういうテキストファイルがあったとします。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot3.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot3.png" alt="screenshot" width="340" height="468" class="alignnone size-full wp-image-13923" /></a>

ごく普通のテキストですが、ところどころに「###」が入っていますね。これが小細工です。

このテキストファイルを「File」>「Import and Split」から取り込みます。Selections are Separated by に「###」を指定するのも忘れずに。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot4.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot4.png" alt="screenshot" width="500" class="alignnone size-full wp-image-13924" /></a>

インポートが完了すると、以下のように３つのファイルが追加されます。当然ように、それぞれのファイルの中身は、テキストファイルの中身と対応しています。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot5.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot5.png" alt="screenshot" width="414" height="286" class="alignnone size-full wp-image-13925" /></a>

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot6.png" alt="screenshot" width="402" height="330" class="alignnone size-full wp-image-13926" /></a>

いちいち分割作業する必要がないので、簡単ですね。

<H3>コピペはつらい</H3>

という機能を踏まえた上で、読み進めてください。

ここ最近「月刊くらした」計画として、毎月一回電子書籍を発行しています。で、そのために過去原稿をEvernoteから探しだし、それをScrivenerに移し替える作業を行っています。コピペで。

短めのエッセイ集なら10回ほどの作業ですが、長くなればなるほどコピペ回数が増え、面倒くささゲージが真っ赤に染まり始めます。

というわけで、上記の「Import and Split」を意識してAppleScriptを書いてみました。

<H3>スクリプトの動作</H3>

まずは機能から。

Evernoteで、ノートを選択。Scrivenerに取り込みたいものを、ぽんぽんとクリックしていきます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot7.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot7.png" alt="screenshot" width="500" class="alignnone size-full wp-image-13927" /></a>

で、スクリプトを起動。

すると、こういうテキストファイルができあがります。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot8.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot8.png" alt="screenshot" width="393" height="259" class="alignnone size-full wp-image-13928" /></a>

ノートごとの

<blockquote>
ノートタイトル
ノートの中身（テキストだけ）

###
</blockquote>

がまとめられたテキストファイルになっています。

あとは、「Import and Split」でそのファイルを取り込めば、作業は完了。

<a href="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/07/screenshot9.png" alt="screenshot" width="402" height="207" class="alignnone size-full wp-image-13929" /></a>

Evernoteのノートを使って、すぐさまScrivenerでプロジェクト管理ができるという、（たぶん私しか使わないでしょうけれども）優れものアプリです。

<H3>中身</H3>
スクリプトは以下。

<script src="https://gist.github.com/rashita/bcbc94ca4009fdff0069.js"></script>

当スクリプトは、全面的に<a href="https://twitter.com/s_z_k_3" target="_blank">@s_z_k_3</a>師匠の「Evernoteのノートをプレーンテキストで取得」スクリプトに依っています。プレーンテキストに変換できさえすれば、いろいろ工夫は広がりますね。

その他、

<a href="http://tonbi.jp/AppleScript/Introduction/12/" target="_blank">エラーに備えよう</a>（鳶嶋工房）
<a href="http://hirakun.blog57.fc2.com/blog-entry-166.html" target="_blank">AppleScriptで扱う日本語（マルチバイト）文字列について</a>（キッズプレート、パスタおかわり）

のページも参考にさせていただきました。

<H3>さいごに</H3>
区切りのための文字や、テキストファイルに書き出す内容（たとえばノートのタイトルを含めるかどうか）など、アレンジする要素はいくつかあります。適当に改造して、お使いください。

まあ、Evernote→Scrivenerの連携を使っている人がどれだけいるかはわかりませんが。