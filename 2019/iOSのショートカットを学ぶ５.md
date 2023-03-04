---
title : iOSのショートカットを学ぶ５
link : 28561
date : Thu, 13 Jun 2019 22:00:19 +0000
categories : ["プログラミング"]
tags : ["ios","iosショートカット"]
draft : false
author : 倉下忠憲
---

前回：<a href="https://rashita.net/blog/?p=28552">iOSのショートカットを学ぶ４</a>

前回までは既存のショートカットの改造を行っていたが、今回からゼロベースでショートカットを組み立てていく。最初の目標は、「FastEverもどき」だ。
<h2>動作の流れ</h2>
まず、流れをイメージしてみよう。

最初にテキストの入力欄が立ち上がって、そこにメモを書き込む。すると、それがEvernoteに送られて新規ノートが作成される。

こういうステップなら良さそうだ。

では、さっそく作ってみよう。
<h2>入力を要求</h2>
まずは、ショートカットを新規作成する。

<a href="https://rashita.net/blog/?attachment_id=28566" rel="attachment wp-att-28566"><img class="alignnone size-large wp-image-28566" src="https://rashita.net/blog/wp-content/uploads/2019/06/226BFABF-B4B2-4187-B322-0B4F03ADA7C9.jpg" alt="" width="329" height="569" /></a>

最初に必要なのは、テキストの入力なので、下の検索ボックスに「入力」と入れてみる。

<a href="https://rashita.net/blog/?attachment_id=28571" rel="attachment wp-att-28571"><img class="alignnone size-large wp-image-28571" src="https://rashita.net/blog/wp-content/uploads/2019/06/A0585F10-A9DB-4240-91AD-57C10E1A34DE.jpg" alt="" width="329" height="569" /></a>

「入力を要求」というのがあったので、それを追加してみる。

<a href="https://rashita.net/blog/?attachment_id=28565" rel="attachment wp-att-28565"><img class="alignnone size-large wp-image-28565" src="https://rashita.net/blog/wp-content/uploads/2019/06/95C7DB6D-38D2-4810-AC3A-091AAF47B180.jpg" alt="" width="329" height="569" /></a><a href="https://rashita.net/blog/?attachment_id=28562" rel="attachment wp-att-28562"><img class="alignnone size-large wp-image-28562" src="https://rashita.net/blog/wp-content/uploads/2019/06/02BF6A93-A03F-4E84-8EB7-51453E49E1A3.jpg" alt="" width="329" height="569" /></a>

無事追加された。上の方にある再生ボタン（右矢印）で実行具合が確認できる。

<a href="https://rashita.net/blog/?attachment_id=28570" rel="attachment wp-att-28570"><img class="alignnone size-large wp-image-28570" src="https://rashita.net/blog/wp-content/uploads/2019/06/656710C4-4598-4521-A40F-CF069686F17A.jpg" alt="" width="329" height="569" /></a>

無事入力欄が立ち上がった。試しに何か入力してみる。

<a href="https://rashita.net/blog/?attachment_id=28567" rel="attachment wp-att-28567"><img class="alignnone size-large wp-image-28567" src="https://rashita.net/blog/wp-content/uploads/2019/06/642F423B-E1F3-4965-B94A-304D9DFAF62A.jpg" alt="" width="329" height="569" /></a><a href="https://rashita.net/blog/?attachment_id=28573" rel="attachment wp-att-28573"><img class="alignnone size-large wp-image-28573" src="https://rashita.net/blog/wp-content/uploads/2019/06/DB46D564-6344-4AA5-8F38-AA0C7C246632.jpg" alt="" width="329" height="569" /></a>

きちんと入力ができていることが確認できた。でもって、ここからもわかるように、入力した結果が、次のアクションに手渡されることになる。

あとは、Evernoteだ。
<h2>Evernoteにノートを作成</h2>
今度は検索ボックスに「Evernote」と入力してみる。

<a href="https://rashita.net/blog/?attachment_id=28563" rel="attachment wp-att-28563"><img class="alignnone size-large wp-image-28563" src="https://rashita.net/blog/wp-content/uploads/2019/06/87D138EB-0F50-4869-B0BC-F25FD41F13CC.jpg" alt="" width="329" height="569" /></a>

いろいろあるが「新規メモを作成」が今回の用途にぴったりだろう。

<a href="https://rashita.net/blog/?attachment_id=28572" rel="attachment wp-att-28572"><img class="alignnone size-large wp-image-28572" src="https://rashita.net/blog/wp-content/uploads/2019/06/C375209E-03F3-4ADB-B602-C944CA8B53E5.jpg" alt="" width="329" height="569" /></a><a href="https://rashita.net/blog/?attachment_id=28569" rel="attachment wp-att-28569"><img class="alignnone size-large wp-image-28569" src="https://rashita.net/blog/wp-content/uploads/2019/06/678EBC19-EACB-447C-AABD-DD537EACED07.jpg" alt="" width="329" height="569" /></a>

ノートタイトルの部分は、デフォルトではオプション（入れても入れなくてもどちらでもOK）となっているが、「無題ノート」だと少し寂しいので、本文と同じものを使用しておく。「入力を要求」となっているのがそれだ。これは「マジック変数」と呼ばれるものだが、ようするにこれ以前のアクションで入力されたデータなどを再利用するためのものである。

もともと本文データは、前のアクション（「入力を要求」）から引き継いで自動的に設定されているのだが、ここではもう一度同じデータ（「入力を要求」）を使用して、それをノートのタイトルに設定している、というわけである。
<h2>実行</h2>
では、これを実行してみよう。

<a href="https://rashita.net/blog/?attachment_id=28568" rel="attachment wp-att-28568"><img class="alignnone size-large wp-image-28568" src="https://rashita.net/blog/wp-content/uploads/2019/06/677E04AD-ACEB-4F72-846E-9904B7ADFB1C.jpg" alt="" width="329" height="569" /></a><a href="https://rashita.net/blog/?attachment_id=28564" rel="attachment wp-att-28564"><img class="alignnone size-large wp-image-28564" src="https://rashita.net/blog/wp-content/uploads/2019/06/90CF3419-4CF4-4B94-AD1D-73ACA766D8E4.jpg" alt="" width="329" height="569" /></a>

メモを入力すると、何事もなく無事に処理が終わった。

で、できたノートが以下である。

<a href="https://rashita.net/blog/?attachment_id=28577" rel="attachment wp-att-28577"><img class="alignnone size-full wp-image-28577" src="https://rashita.net/blog/wp-content/uploads/2019/06/screenshot-2.png" alt="" width="576" height="480" /></a>

完璧だ。たった二つのアクションをつなげるだけで、Evernoteへの簡易送信ショートカットが完成してしまった。ちょっと驚くくらいである。

とは言え、現状だと、ちょっとしたメモくらいならばいいのだが、複数行にわたる長大なメモを書いてしまうと、ノートタイトルがえらいことになってしまう。

<a href="https://rashita.net/blog/?attachment_id=28578" rel="attachment wp-att-28578"><img class="alignnone size-full wp-image-28578" src="https://rashita.net/blog/wp-content/uploads/2019/06/screenshot-3.png" alt="" width="571" height="340" /></a>

できれば、本文の一行目だけをタイトルに使用したい。さて、どうすればいいだろうか。それについては次回までの課題としておこう。