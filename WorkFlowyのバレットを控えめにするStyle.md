---
title : WorkFlowyのバレットを控えめにするStyle
link : 24667
date : Fri, 04 May 2018 02:30:54 +0000
categories : ["0-知的生産の技術","アウトライナーで遊ぼう"]
tags : ["stylish","workflowy"]
draft : false
author : 倉下忠憲
---

Firefoxのブラウザ拡張「Stylish」を使います。

通常のWorkFlowyはこんな感じ。

<a href="https://rashita.net/blog/?attachment_id=24668" rel="attachment wp-att-24668"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-6.png" alt="" width="958" height="685" class="alignnone size-full wp-image-24668" /></a>

ちょっとBarrettがくどいですね。これを以下のようにします。

<a href="https://rashita.net/blog/?attachment_id=24669" rel="attachment wp-att-24669"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-7.png" alt="" width="969" height="677" class="alignnone size-full wp-image-24669" /></a>

かなり控えめになりました。カロリー50%オフ。

設定は以下の通り。

[css]
.bullet, #bulletBucket .bulletBucketBullet {
    height: 9px;
    width: 9px;
    opacity:0.5;
   }

.selected &gt; .children &gt; .project .project &gt; .name &gt; .bullet {
    margin-top: 9px;
}

.selected &gt; .children &gt; .project &gt; .name &gt; .bullet {
    margin-top: 9px;
}

.bullet {
    left: 60px;
}

.children {
    border-left: 0px solid #eee;
}
[/css]

Barrettを小さくしたついでに、項目の横に出てくる縦線も消しました。

※この線を消しました
<a href="https://rashita.net/blog/?attachment_id=24671" rel="attachment wp-att-24671"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-8.png" alt="" width="341" height="289" class="alignnone size-full wp-image-24671" /></a>

もし、項目ごとの区切りがもう少し欲しいな、という場合は、border-left: 0px solid #eee;の下に、border-bottom: 1px solid #eee;を追加してください。罫線っぽいものが追加されます。

<a href="https://rashita.net/blog/?attachment_id=24673" rel="attachment wp-att-24673"><img src="https://rashita.net/blog/wp-content/uploads/2018/05/screenshot-9.png" alt="" width="920" height="625" class="alignnone size-full wp-image-24673" /></a>

もっと濃い色の罫線が欲しい場合は、border-bottom: 1px solid black;とでもするか、カラーコードを検索して使いたい色を探してみてください。

では、では。

