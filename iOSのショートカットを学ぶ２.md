---
title : iOSのショートカットを学ぶ２
link : 28517
date : Mon, 10 Jun 2019 22:00:38 +0000
categories : ["プログラミング"]
tags : ["ios","iosショートカット"]
draft : false
author : 倉下忠憲
---

前回:<a href="https://rashita.net/blog/?p=28503">iOSのショートカットを学ぶ１</a>

まず、めちゃくちゃ簡単な「改造」からやってみよう。

使うのは「サングラスをかける」。ギャラリーの検索ボックスに「サングラス」と入れれば出てくるだろう。

<a href="https://rashita.net/blog/?attachment_id=28519" rel="attachment wp-att-28519"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/AE37C572-0509-4603-BDC6-06D1799F4AA1.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28519" /></a>

まずは、これを取り込む。

※「ショートカットを取得」を押す
<a href="https://rashita.net/blog/?attachment_id=28520" rel="attachment wp-att-28520"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/0E173AC1-6075-4994-87CA-F45958DCB154.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28520" /></a>

その後、試しに実行してみよう。

※灰色の「サングラスをかける」を押せばこのショートカットが実行される
<a href="https://rashita.net/blog/?attachment_id=28522" rel="attachment wp-att-28522"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/AB6E195F-7000-4388-94FF-8BE146C89FB2.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28522" /></a>

<h2>「サングラスをかける」の実行</h2>

※設定を入力
<a href="https://rashita.net/blog/?attachment_id=28524" rel="attachment wp-att-28524"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/90C4F714-AF36-4C95-AEFE-948A8F97DF45.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28524" /></a>

※落ちを入力
<a href="https://rashita.net/blog/?attachment_id=28525" rel="attachment wp-att-28525"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/D36E3D3C-341D-4290-8D0A-CF588884AFE0.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28525" /></a>

※「クリップボードにコピー」を選択
<a href="https://rashita.net/blog/?attachment_id=28526" rel="attachment wp-att-28526"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/10E11B68-FA59-4DB3-95C6-94133F253E01.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28526" /></a>

すると、以下のような文字列がクリップボードにコピーされる。

<code>
夏の盛り

(•_•)

( •_•)>⌐■-■

(⌐■_■)

前が見えない
</code>

くだらなさについては横に置いてもらうとして、動作はわかりやすいだろう。二回のテキストの入力があり、それをバンズにして一連の文章が形成される。真ん中の顔文字の部分は定型であり、ネタツイートを作るときに活躍することが予想される。

では、この中身を少し覗いてみよう。

<h2>解体新書</h2>

<a href="https://rashita.net/blog/?attachment_id=28527" rel="attachment wp-att-28527"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/F8AAEB0C-73D4-43FE-91DA-D47C8D5BD790.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28527" /></a>

まず、ユーザーにテキストの入力が要求される。「設定は何ですか？」というダイアログによってそれが伝えられる。その入力結果が、「Setup」という名前の変数に放り込まれる。これ以降、この「Setup」を参照すると、ユーザーが入力した「設定は何ですか？」への答えが飛び出てくる。

<a href="https://rashita.net/blog/?attachment_id=28528" rel="attachment wp-att-28528"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/33BA7CA1-C4E8-4BF1-AD82-942B010110E8.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28528" /></a>

こちらも動作は同じ。「設定」ではなく「落ち」になっていて、放り込まれる変数が「Punchline」となっている点だけが違いだ。

続いて「テキスト」

<a href="https://rashita.net/blog/?attachment_id=28529" rel="attachment wp-att-28529"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/1C9A0A58-31DC-474F-A61D-458884A6D725.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28529" /></a>

<a href="https://rashita.net/blog/?attachment_id=28531" rel="attachment wp-att-28531"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/B60607FA-D8DD-4406-89EA-C89D3923EBDA.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28531" /></a>

サングラスの顔文字の上下に、「Setup」と「Punchline」がやや特殊な形で記述されている。こうすることで、ユーザーが入力した中身を取り出せるわけだが、今のところは深く考えなくてもいい。データの流れだけを確認していこう。

「テキスト」の下には、「メニューから選択」がある。ここで「共有」と「クリップボードにコピー」が設定されている。まさしくさきほど選んだやつだ。

<a href="https://rashita.net/blog/?attachment_id=28529" rel="attachment wp-att-28529"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/1C9A0A58-31DC-474F-A61D-458884A6D725.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28529" /></a>

その下には、それぞれのメニューの選択結果に合わせたオプションが指定されている。

<a href="https://rashita.net/blog/?attachment_id=28530" rel="attachment wp-att-28530"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/05E25A9B-B6AA-4118-9269-D8E3363EFA04.jpg" alt="" width="320" height="568" class="alignnone size-large wp-image-28530" /></a>

この辺も特に難しいことはないだろう。

さて、ここで問題である。クリップボードに貼り付けられる顔文字を、

<code>
(•_•)

( •_•)>⌐■-■

(⌐■_■)
</code>

から、

<code>
(•_•)

( •_•)>⌐□-□

(⌐□_□)
</code>

に変えるには、どの部分を変更すればいいだろうか。

そう難しくはないと思うが、本稿の手順を一通りなぞって、自分でやってみて欲しい。

答えは次回。