---
title : 7wrinerの独特なwindow機能
link : 24434
date : Tue, 10 Apr 2018 01:26:02 +0000
categories : ["0-知的生産の技術"]
tags : ["7wriner"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=24377" title="7wrinerのその他の機能 – R-style">前回</a>は、7wrinerの保存・出力まわりの機能を紹介しました。

今回は、一番最後に実装したウィンドウ機能を紹介します。

<h3>it is window</h3>

Macだと、shitf + command + →で（winならshift + alr + →で）、ぴょこんとウィンドウが開きます。imaginary windowという仮想的な窓です。

<a href="https://rashita.net/blog/?attachment_id=24435" rel="attachment wp-att-24435"><img src="https://rashita.net/blog/wp-content/uploads/2018/04/screenshot-57.png" alt="" width="1032" height="707" class="alignnone size-full wp-image-24435" /></a>

ここはメインラインとは別のカード置き場です。つまり、カードをドラッグできます。

<a href="https://gyazo.com/5bb526c510f6501183c4560562ffd284"><img src="https://i.gyazo.com/5bb526c510f6501183c4560562ffd284.gif" alt="https://gyazo.com/5bb526c510f6501183c4560562ffd284" width="952"/></a>

でもって、入れたカードに対して、特別なコマンドが使えるようになります。

逆順に並び替えたり、ランダムに並び替えたり、

<a href="https://gyazo.com/9a314e557d06e8559a1016d0b782d30c"><img src="https://i.gyazo.com/9a314e557d06e8559a1016d0b782d30c.gif" alt="https://gyazo.com/9a314e557d06e8559a1016d0b782d30c" width="532"/></a>

気に入った順番になったらマージもできます。

<a href="https://gyazo.com/1e831c81875f19ac7a250e547db551b1"><img src="https://i.gyazo.com/1e831c81875f19ac7a250e547db551b1.gif" alt="https://gyazo.com/1e831c81875f19ac7a250e547db551b1" width="568"/></a>

むろんそのカードをラインに戻すこともできます。

<a href="https://gyazo.com/54cc8c32ec9d9742c767f4f21e27f01a"><img src="https://i.gyazo.com/54cc8c32ec9d9742c767f4f21e27f01a.gif" alt="https://gyazo.com/54cc8c32ec9d9742c767f4f21e27f01a" width="824"/></a>

つまり、このimaginary window（以下iw）は、小さなまな板でありボウルです。

縦に長く伸びたラインから、そのとき「調理」したいものだけをこのiwにドラッグする。で、マージなり入れ換えなりをして、元のラインに戻す。

しかも、このiwは、fixされているので、メインのラインを移動しても残り続けます。つまり、Aというラインから別のBというラインにカードを大量移動させるときにも利用可能です（マージせずに戻す場合は、recallボタンを押すと手間が大いに省けます）。

このiwは、縦になが〜〜〜〜く伸びたアウトライナーを触っているときに常々あったらいいなと思っていた機能を実装しました。だから、かなり実践的というか実際的な機能だと思います。とは言え、Macのfirefox以外でどう動くかは検証していませんのであしからず。

<h2>他のモードのwindow</h2>

で、上のwindowを実装したら、「別のモードでもwindow表示されたらどうなる？」と閃いて、それもやってみました。

プレビューモードでwindowを表示させると、総文字数とindexが表示されます。このindexにピックアップされるのは行頭に # がいくつかついている行のことです。

で、これはindexですので、当然文章内リンクとして機能します。つまりクリックすると表示が該当箇所に飛びます。

<a href="https://gyazo.com/86f106d34cd4f9d18ccb94a957d53eee"><img src="https://i.gyazo.com/86f106d34cd4f9d18ccb94a957d53eee.gif" alt="https://gyazo.com/86f106d34cd4f9d18ccb94a957d53eee" width="708"/></a>

では、オーバービューモードではどうなるか。

<a href="https://gyazo.com/3576c444ee376f77c32cf22fa1687945"><img src="https://i.gyazo.com/3576c444ee376f77c32cf22fa1687945.gif" alt="https://gyazo.com/3576c444ee376f77c32cf22fa1687945" width="880"/></a>

クリックしたカードの詳細が表示されます。オーバービューモードでは長いカードは割愛されて表示されるので、その中身を知りたくなったときに使えます。

7wrinerには、もう一つモードがあったのをご記憶でしょうか。そう、フルスクリーンモードです。

フルスクリーンモードでは、設定のためのwindowが表示されて、現在は背景色とテキスト文字が設定できます。

<a href="https://gyazo.com/519dfbe30a9d399801b127fa7032fc51"><img src="https://i.gyazo.com/519dfbe30a9d399801b127fa7032fc51.gif" alt="https://gyazo.com/519dfbe30a9d399801b127fa7032fc51" width="804"/></a>

そして、ここで力つきました。

<h2>まとめ</h2>

7wrinerには補助的なwindow機能があるのですが、ご覧のように基本的にはパソコンで操作するための機能です。なにせラインに重ねあわせて表示されるので画面が狭いとなんじゃこりゃ、ってことになりかねませんからね。これについては、私が基本的にパソコンで作業をする人間であり、その人間に最適化して作ったからこうなったとご理解ください。

とりあえず、いろいろなモードでのウィンドウがありますが、やはりiwが一番便利です。こういう「一時操作のための場所」は、断片を扱うツールでは必須だと思います。



