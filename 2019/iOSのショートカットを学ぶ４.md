---
title : iOSのショートカットを学ぶ４
link : 28552
date : Wed, 12 Jun 2019 22:00:51 +0000
categories : ["プログラミング"]
tags : ["ios","iosショートカット"]
draft : false
author : 倉下忠憲
---

前回：<a href="https://rashita.net/blog/?p=28541">iOSのショートカットを学ぶ３</a>

さて、前回の解答からである。

答えは、シンプルだ。「次の場合」の中にもう一つの「次の場合」を入れる。そうすることで、「http://が含まれているかどうか」を判断した後で、「https://が含まれているかどうか」を確認できる。

アクションの流れは以下の通り。

<a href="https://rashita.net/blog/?attachment_id=28554" rel="attachment wp-att-28554"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/1F4E374C-4750-4E8F-B762-FF553CF8D4E3.jpg" alt="" width="640" height="1136" class="alignnone size-full wp-image-28554" /></a>

<a href="https://rashita.net/blog/?attachment_id=28555" rel="attachment wp-att-28555"><img src="https://rashita.net/blog/wp-content/uploads/2019/06/D4C11DB9-2A3A-4201-A21C-F9B4F83353F0.jpg" alt="" width="640" height="1136" class="alignnone size-large wp-image-28555" /></a>

ようするに、あれである。「入れ子状」というやつだ。丁寧に追いかければ、

http://が含まれている？
　Yes→データを次のアクションに渡す
　No→http://が含まれている？
　　Yes→データを次のアクションに渡す
　　No→クリップボードを取得する

という形になっている。もちろん、将来Httpzみたいなものが出てきたときは、さらに入れ子状にして判断を三段重ねにすることもできる。

この「次の場合」の入れ子状が使えるようになれば、ややこしい状態も管理できるようになる。もちろん、その分ショートカットの中身もややこしくなるわけだが、それは受け入れるしかないだろう。

というわけで、これで「次の場合」がかなり使えるようになったと思う。もう一つ、プログラミング的な要素として「繰り返す」というのがあるのだが、それはまた実例が出てきたときにでも紹介するとしよう。

というわけで、「ギャラリーにあるものを、それなりに改造して使えるようにする」の初歩についてはいったんここまでにしておく。次回は、ゼロベースで自分のショートカットを作ってみよう。

お題は、「FastEverっぽいショートカット」である。もし組めるなら、ぜひ自分で組んでみて欲しい。
