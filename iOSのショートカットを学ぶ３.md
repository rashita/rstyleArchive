---
title : iOSのショートカットを学ぶ３
link : 28541
date : Tue, 11 Jun 2019 22:00:18 +0000
categories : ["プログラミング"]
tags : ["ios","iosショートカット"]
draft : false
author : 倉下忠憲
---

前回:<a href="https://rashita.net/blog/?p=28517">iOSのショートカットを学ぶ２</a>

まずは、前回の課題の答えから。

正解は、5個目に出てくるアクション「テキスト」の中身を

<code>(•_•)

( •_•)>⌐■-■

(⌐■_■)</code>

から

<code>(•_•)

( •_•)>⌐□-□

(⌐□_□)</code>

に書き換えればいい。簡単だっただろうが、ともかく一度自分で書き換えてみることが大切である。

<h2>「後で読む」の改造</h2>

さて、今回の「改造」は、「後で読む」を使う。ギャラリーで検索すれば出てくる。中身はこんな感じ。

<a href="https://rashita.net/blog/?attachment_id=28542" rel="attachment wp-att-28542"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/D4D733B5-3317-448D-8750-7DF23ED84C82.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28542" /></a>

細かくは自分で確認してもらうとして、今回はいきなりこれを使ってみる。Safariを立ち上げ、何か適当なページ（このページでもいい）を開いて、このショートカットを発動させる。

※共有メニューの「ショートカット」から発動可能
<a href="https://rashita.net/blog/?attachment_id=28547" rel="attachment wp-att-28547"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/32EA5E03-2B9E-4AC0-95F4-7246FD4EE02F.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28547" /></a>

すると、選択肢が出てくるので「リーディングリスト」を選択する。「リンクが保存されました！」となれば、当面はOKだ。

その後、Safariでリーディングリストを開いてみよう。Safariの下メニューにある本を開いたアイコンのボタンがそれだ。どうだろうか、うまく開いていたページが保存されていただろうか。

場合によって、ここは分かれる。もし、このページや、URLがhttps://ではじまるページならば、ページは<strong>保存されていない</strong>はずである。逆に、http://で始まるページならば、うまく保存されているだろう。

ここが今回の改造ポイントだ。

<h2>s一個だけの違い</h2>

では、「後で読む」ショートカットの中身を覗いてみよう。

<a href="https://rashita.net/blog/?attachment_id=28542" rel="attachment wp-att-28542"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/D4D733B5-3317-448D-8750-7DF23ED84C82.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28542" /></a>

ストレートに読めば、「Input」という名前の変数にhttp://という文字列が「含まれている」場合、なんらかの処理が行われることがわかる。

それはいいのだが、たとえば、このページのURLの先頭は、https://である。で、この二つ（http://とhttps://）は、一見よく似ているが、プログラム側から見れば、別の文字列いなる。だから、「http://が含まれてるかな〜、う〜ん、ないな、じゃあパス」みたいなことになって、綺麗にスルーされる。なかなか融通が効かないのだが、その辺は人間側が合わせるしかない。

となると、このショートカットを、https://でも使えるようには、少しの「改造」が必要である。

さて、どうするか。

望ましい動作としては、プログラム君が「http://かhttps://が含まれてるかな〜」と探してくれればいい。あるいは、http://を探したあとに、https://を探してくれてもいい。

それを踏まえた上で、この「次の場合」がどういうものなのかを見ていこう。

<h2>「次の場合」</h2>

<a href="https://rashita.net/blog/?attachment_id=28542" rel="attachment wp-att-28542"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/D4D733B5-3317-448D-8750-7DF23ED84C82.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28542" /></a>

まず、冒頭で何かしらをinputという変数に放り込んでいる。これは、safariを開いているときなどは、そのページのURLがそこに設定されていると、とりあえずは理解しておく。

で、それが本当にURLなのかどうかを、この「次の場合」で確かめている。確かめ方は簡単で、その中身にhttp://が含まれているかどうかで判断する。

もし含まれていれば、そのままその中身を次のアクションに手渡す。

<a href="https://rashita.net/blog/?attachment_id=28544" rel="attachment wp-att-28544"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/2C7606FA-521F-4022-A55B-55720DB656FF.jpg" alt="" width="320" height="568" class="alignnone size-full wp-image-28544" /></a>

含まれていないときは、クリップボードの中身を次のアクションに手渡す。ということは、ページを開いていないときでも、何かURLをコピーした後に、このショートカットを発動すると、それをリーディングリストに送り込める、という寸法である。

このように「次の場合」というのは、ある条件を満たすときに行う動作と、満たさないときに行う動作を分けることができる。プログラミングっぽく言えば、条件分岐、というやつだ。

この処理のおかげで、かなり複雑なことができるのだが、現状は「http://」だけしか探してくれないので、「https://」の場合はそれに合致せず、クリップボードがコピーされてしまう、という問題が生じている。

さて、ここで課題である。このショートカットの通常の動作に加えて「https://」のページでもきちんとリーディングリストに保存されるようにするには、どう「改造」すればいいだろうか。

一応、ヒントを言えば、新しい道具立ては必要ない。この記事にある情報だけで「改造」はできるはずだ。ただしこれは（前回に比べれば）ちょっとだけ難しいかもしれない。

解答は次回に載せるので、それまではちょこちょこ自分で改造してみてほしい。
