---
title : 物書きが使うVS Code 〜執筆に嬉しい機能〜
link : 30341
date : Wed, 02 Sep 2020 05:33:50 +0000
categories : ["物書き生活と道具箱"]
tags : ["vs-code","物書きが使うvs-code"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=30307">物書きが使うVS Code　〜インストールと日本語表示化〜</a>
<a href="https://rashita.net/blog/?p=30312">物書きが使うVS Code　〜画面構成〜</a>
<a href="https://rashita.net/blog/?p=30321">物書きが使うVS Code 〜Workspace〜</a>
<a href="https://rashita.net/blog/?p=30332">物書きが使うVS Code　〜カスタマイズと設定項目〜</a>

今回は、執筆時に嬉しい機能をいくつか紹介します。ちょっとした機能ですが、地味に役立ちます。

<h2>マークダウンと開閉</h2>

拡張子が.mdのファイルは、マークダウンモードで開きます。

で、たとえば、「#」とかを行頭に入力して、半角スペースを入れると、その行が見出しとして認識されます。これはまあ、よくある機能ですね。

<a href="https://rashita.net/blog/?attachment_id=30345" rel="attachment wp-att-30345"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-5.png" alt="" width="694" height="712" class="alignnone size-full wp-image-30345" /></a>

で、その見出し行の横にカーソルを持っていくと、下向きの矢印が表示されます。なんとなくわかりますね。クリックすれば、下位の要素が閉じてくれるのです（collapse）。もちろん、もう一回クリックすれば、下位要素が開きます（expand）。

<a href="https://gyazo.com/657bc0534c01ab9b528aa284399ee3ac"><video alt="Video from Gyazo" width="392" autoplay muted loop playsinline controls><source src="https://i.gyazo.com/657bc0534c01ab9b528aa284399ee3ac.mp4" type="video/mp4" /></video></a>

いちいちマウスでカーソル移動するのが面倒ならば、option + command + [ （または]）のショートカットでも開閉できます。

一回キー操作が多くなりますが、command + k → command + l だと、開閉のトグルとなります。閉じていたら開く、開いていたら閉じるです。

この「アウトライナーじゃなくてエディタなんだけど、項目が開閉できる」点が、私がVS Codeをすごく気に入っている点の一つです。普通に文章を書いているときでもあるんですよね、「ここは今閉じておきたい」みたいな感じが（たとえば本文中に差し込まれているコラムとか）。

アウトライナーのように階層を作り、本文をその下位レベルに移動させなくても、その上の行に見出しを追加すれば、簡単に開閉ができるようになります。org-modeっぽい感じです（本家ほどではありませんが）。

ちなみに、.mdファイルでなくても、右下のモードを表示をクリックすれば、任意のモードに変換できますので、.txtファイルであっても、マークダウンモードに切り替えれば上記の操作は可能となります。

<a href="https://rashita.net/blog/?attachment_id=30346" rel="attachment wp-att-30346"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-6.png" alt="" width="422" height="234" class="alignnone size-full wp-image-30346" /></a>

<h2>マークダウンプレビュー</h2>

マークダウンが書けるなら、プレビューも表示させたいところですね。ご安心ください。 command + k → v で分割ウィンドウにプレビュー表示が開きます。

<a href="https://rashita.net/blog/?attachment_id=30347" rel="attachment wp-att-30347"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-7-700x538.png" alt="" width="700" height="538" class="alignnone size-large wp-image-30347" /></a>

で、このプレビュー表示に関しても、カスタマイズが可能です（詳しくはgoogle.comへ）。

<h2>zen mode</h2>

似たショートカットキーとして、command + k → zがあります。

これを押すと、開くのです。zenモードへの扉が。

<a href="https://rashita.net/blog/?attachment_id=30348" rel="attachment wp-att-30348"><img src="https://rashita.net/blog/wp-content/uploads/2020/09/screenshot-8-700x438.png" alt="" width="700" height="438" class="alignnone size-large wp-image-30348" /></a>

エディタ以外の要素が隠され、行番号とかも消えちゃいます。ザ、集中空間ですね。私は、本の執筆ではだいたいこのモードを使っています。

ちなみに、esc → esc で通常空間に戻れます。

<h2>さいごに</h2>

他にもわんさかショートカットキーはあるのですが、とりあえず、 command + b でサイドバーがトグルすることを覚えておけば十分でしょう（たぶん）。

ともあれ、以上のように、VS Codeは物書き用のエディタとしても十分威力を発揮してくれます。すげーやつです。