---
title : 物書きが使うVS Code　〜豆技10選〜
link : 30364
date : Tue, 08 Sep 2020 05:40:10 +0000
categories : ["物書き生活と道具箱"]
tags : ["vs-code","物書きが使うvs-code"]
draft : false
author : 倉下忠憲
---

べっ、べつに、この原稿を膨らませて本を書こうとしているわけじゃないんだからね！

みたいなタイトルですが、気にしないでください。これまで連載を書いてきて、「あっ、これ書き忘れた！」みたいなものを後からいくつか発見したので、それを紹介しておきます。

<strong>▼これまでの連載：</strong>
<a href="https://rashita.net/blog/?p=30307">物書きが使うVS Code　〜インストールと日本語表示化〜</a>
<a href="https://rashita.net/blog/?p=30312">物書きが使うVS Code　〜画面構成〜</a>
<a href="https://rashita.net/blog/?p=30321">物書きが使うVS Code 〜Workspace〜</a>
<a href="https://rashita.net/blog/?p=30332">物書きが使うVS Code　〜カスタマイズと設定項目〜/a>
<a href="https://rashita.net/blog/?p=30341">物書きが使うVS Code 〜執筆に嬉しい機能〜/a>
<a href="https://rashita.net/blog/?p=30352">物書きが使うVS Code 〜拡張機能〜</a>



<h2>マルチカーソル</h2>

option + command + ↑↓ でカーソルが伸びます。複数行に同一の操作をするときに抜群に便利です。

<a href="https://gyazo.com/3461af9ff7cb08760b57c10567b3c03c"><video alt="Video from Gyazo" width="508" autoplay muted loop playsinline controls><source src="https://i.gyazo.com/3461af9ff7cb08760b57c10567b3c03c.mp4" type="video/mp4" /></video></a>

<h2>行移動のショートカット</h2>

option + ↑↓ でカーソル行を上下に移動できます。

ちなみに、 shift + option + ↑↓だと、カーソル行の複製です。

<h2>Explorerからファイルを開く</h2>

shift + command + e でExplorerにフォーカスが移動します。

で、開きたいファイルにカーソルを合わせたら、spaceでファイルが開きます。

あるいは、control + enter ならウィンドウを分割してファイルが開きます。

<h2>ウィンドウ移動のショートカット</h2>

control + tabで、開いているタブを移動します。

<h2>クイックオープン</h2>

command + pで、Quick Openのウィンドウが開きます。一度利用したファイルなどは、ここから開くと便利です。

あと、shift + command + p にすると、「>」を入力した状態でウィンドウが開き、そのままコマンドを探すことができます。で、だいたいのことはここでできます。git系のコマンドもあります。

もちろん、command + pをしてから自分で「>」を入力しても同じことです。

<h2>Searchのショートカット</h2>

shift + command + fでSearchにフォーカスが移動します。

ワークスペース内のファイルにgrep検索を実行してくれます。極めて便利です。

<a href="https://rashita.net/blog/?attachment_id=30367" rel="attachment wp-att-30367"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-14.png" alt="" width="416" height="1688" class="alignnone size-full wp-image-30367" /></a>

検索結果をエディタで開くこともできます。

<a href="https://rashita.net/blog/?attachment_id=30368" rel="attachment wp-att-30368"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-15-700x501.png" alt="" width="700" height="501" class="alignnone size-large wp-image-30368" /></a>

<h2>移動のショートカット</h2>

control + q で、いろいろな場所にフォーカスを移動できます。

<h2>ショートカット一覧</h2>

というように、ショートカットキーは盛りだくさんなのですが、

command + k → command + s

で、一覧できます。キーワードで絞り込むことも可能です。一度ざっと眺めておくとよいでしょう。

<h2>gitの設定（コミットしたら、プッシュする）</h2>

どうせコミットしたら、すぐにプッシュするんだから、勝手にやっといて、という設定が可能です。

「git post」あたりで絞り込めると思います。

<a href="https://rashita.net/blog/?attachment_id=30369" rel="attachment wp-att-30369"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-16-700x189.png" alt="" width="700" height="189" class="alignnone size-large wp-image-30369" /></a>

settings.jsonに書くなら、

"git.postCommitCommand": "push",

です。 

<h2>Explorerの段差</h2>

標準表示だと、Explorerの段差が少し狭くて、わかりにくいことがあります。これも設定できます。

勘のいい人なら、settingsで「indent」で絞り込めばいいんじゃね？　と思われるでしょうが、その通りです。

<a href="https://rashita.net/blog/?attachment_id=30370" rel="attachment wp-att-30370"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-17.png" alt="" width="566" height="328" class="alignnone size-full wp-image-30370" /></a>

settings.jsonに書くなら、

"workbench.tree.indent": 14,

です（数字は適当に）。

<h2>さいごに</h2>

以上、VS Codeの細かいあれこれでした。

ともかく、いろいろできるので、森というか沼は深いです。