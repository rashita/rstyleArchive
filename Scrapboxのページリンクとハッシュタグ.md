---
title : Scrapboxのページリンクとハッシュタグ
link : 29788
date : Tue, 17 Dec 2019 08:03:47 +0000
categories : ["scrapboxの用法"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

Scrapboxには、プロジェクト内リンクを作る方法が二種類あります。一つは、[]（ブラケット）で囲むもの。もう一つはあたまに#をつけるものです。

あたまに#をつけるものは、他のツールではハッシュタグと呼ばれているので、ここでもそれに習うことにしますが、Scrapboxにおいて、この[hogehoge]と#hogehogeは、ほとんどまったく同じものです。

つまり、以下の二つは（ほぼ）同じように機能します。

<img class="is-slide lazyloaded" src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938313/picture_pc_f15a8ead83a239e277bc332f38ee1ab2.png" alt="画像1" data-src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938313/picture_pc_f15a8ead83a239e277bc332f38ee1ab2.png" />

ただし、ご覧のように文章の中に#が入っていると微妙に違和感がありますね。ほとんどの単語にハッシュタグをつけることに慣れているインスタグラー以外なら、上の方が書きやすい（＆読みやすい）でしょう。

とりあえず、どちらも同じなので、どちらを使うかはまったく個人の自由です。

一点だけ違いがあるとすれば、この二つは当てられているtypeが異なっているので、UserCSSでカスタマイズするときに異なるCSSを当てられる、くらいのことを意識しておけば十分でしょう。

<img class="is-slide lazyloaded" src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938434/picture_pc_a03ebc655fb9005a812b4d006d18fdbd.png" alt="画像2" data-src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938434/picture_pc_a03ebc655fb9005a812b4d006d18fdbd.png" />

<img class="is-slide lazyloaded" src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938439/picture_pc_8f8ab1d4ecdb341c2d74b709ed276987.png" alt="画像3" data-src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938439/picture_pc_8f8ab1d4ecdb341c2d74b709ed276987.png" />
<h3>実体ページと未実体ページ</h3>
上の話は、「ぶっちゃけどっちでもいい」という話に落ち着くのですが、押さえておきたいのは次の違いです。

Scrapboxの同一プロジェクト内別ページへのリンク（以下ページリンクと呼称）は、まず二種類の色をもちます。青字と赤字です。

<img class="is-slide lazyloaded" src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938574/picture_pc_4220ce3782556e2f71deb087e6233562.png" alt="画像4" data-src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938574/picture_pc_4220ce3782556e2f71deb087e6233562.png" />

青字がすでに存在しているページで、赤字がまだ存在していないページ、というのが簡単な理解なのですが、それだけではありません。まだ存在していないページ（以下未実体ページと呼称）であっても、青字になる場合があるのです。

たとえば、上の「断片からの要請」をクリックしてみると、以下のページが表示されます。

<img class="is-slide lazyloaded" src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938654/picture_pc_b713f697e4c6d57c05cd6d8b6e9bce4f.png" alt="画像5" data-src="https://d2l930y2yx77uc.cloudfront.net/production/uploads/images/16938654/picture_pc_b713f697e4c6d57c05cd6d8b6e9bce4f.png" />

ページの中身は存在していません。未実体ページです。でも、このページへのリンクは青字になっているのです。なぜかと言えば、同じページに言及している他のページがあるからです（Linksに表示されていますね）。

つまり、未実体ページであっても、複数のページから言及されているならば、そのリンクは青字になる、ということです。
<h3>青字になっている意味</h3>
このことは何を意味するのでしょうか。リンクが赤字になっているというのは、「未実体ページ」であり、これから中身を書いてくださいねと誘い込むようなニュアンスを帯びています。

しかし、そのページが複数のページからリンクされると赤字ではなくなるのです。つまり、誘い込むようなニュアンスは失われます。これが何を意味するのかと言えば、「そういうページがあってもいいよね」という運営側の思惑がある、ということです。

たとえば、美味しいラーメン屋を集めているプロジェクトがあるとして、そこに地域名を入力していったとしましょう。たとえば[東京]のような形です。

当然このような[東京]は、他のページにもたくさん現れることでしょう。つまり、青字になります。

では、その「東京」という未実体ページは、中身が書かれるべきでしょうか。
<blockquote>東京（とうきょう）とは、日本の関東平野中央部の東京湾に面する世界最大級のメトロポリスであり、日本の事実上の首都である。現在、東京には23特別区・26市・5町・8村の基礎自治体がある。
Wikipedia-東京 <a href="https://ja.wikipedia.org/wiki/%E6%9D%B1%E4%BA%AC" target="_blank" rel="noopener noreferrer">https://ja.wikipedia.org/wiki/%E6%9D%B1%E4%BA%AC</a></blockquote>
みたいなことを書き込んだとき、そのラーメンプロジェクトにハッピーさがアップするでしょうか。おそらく否でしょう。

つまり、キーワードの中には、わざわざ説明を入れる必要がない、ただページとページをつなぐだけのものがあっても全然構わない、ということなのです。だから、Scrapboxでは、未実体のページでも青字になっているのでしょう。
<h3>まとめ</h3>
説明を入れる必要がないページは、他の情報整理ツールでは「タグ」や「カテゴリ」として扱われます。

しかし、Scrapboxはすべてが「ページ」なので、その表現は未実体ページとなります。それは、他のオレンジ色リンクの「これから内容が書かれる」未実体ページとは、また異なった役割を持っているのです。

その意味で、Scrapboxにはハッシュタグというものはありません。[hogehoge]と#hogehogeは、どちらもページリンクであり、その機能は同一です。

しかし、Scrapboxには、実体ページと未実体ページがあります。そしてその未実体ページにも、「これから内容が書かれるページ」と「今後も内容は書かれない（であろう）ページ」があるわけです。

で、その後者をあえて名付けるなら「ハッシュタグページ」となるでしょう。とは言え、別にそのページへのリンクを#hogehogeとする必要はありません。[hogehoge]でも十分機能します。もちろん、はっきり明示するために#hogehogeとしたって大丈夫なわけですが。