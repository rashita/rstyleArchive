---
title : ブクログのブックマークレットを改良してKindle本も登録できるように
link : 26122
date : Thu, 08 Nov 2018 01:04:50 +0000
categories : ["物書き生活と道具箱"]
tags : ["javascript","ブクログ","ブックマークレット"]
draft : false
author : 倉下忠憲
---

ブクログには、Amazonページから簡単に登録できるブックマークレットが準備されています。

<a href="https://booklog.jp/bookmarklet">ブックマークレット</a>

で、このブックマークレットはとても便利なのですが、残念ながらKindle本に対応していません。

以下のページで発動すると、

<a href="https://rashita.net/blog/?attachment_id=26123" rel="attachment wp-att-26123"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-41.png" alt="" width="813" height="376" class="alignnone size-full wp-image-26123" /></a>

空っぽの検索結果が返ってきます。

<a href="https://rashita.net/blog/?attachment_id=26124" rel="attachment wp-att-26124"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-42.png" alt="" width="794" height="567" class="alignnone size-full wp-image-26124" /></a>

どうやら、紙の本のページとKindle本のページでは、ASINを取得するためのElementが異なる様子。

そこで、少し書き換えたものを用意しました。

<a href="https://scrapbox.io/rashitamemo/%E3%83%96%E3%82%AF%E3%83%AD%E3%82%B0%E3%81%AE%E3%83%96%E3%83%83%E3%82%AF%E3%83%9E%E3%83%BC%E3%82%AF%E3%83%AC%E3%83%83%E3%83%88">ブクログのブックマークレット - 倉下忠憲の発想工房</a>

[code]javascript:var%20d=document,w=window,g=d.getElementById('ASIN');if(!g)var%20g=d.getElementsByName('ASIN.0')[0];var%20e=w.getSelection,k=d.getSelection,x=d.selection,s=(e?e():(k)?k():(x?x.createRange().text:0)),f='http://booklog.jp/blet',l=d.location,a=(g?g.value:''),e=encodeURIComponent,p='?v=2&amp;u='+e(l.href)+'&amp;s='+e(s)+'&amp;a='+e(a),u=f+p,a=function(){w.open(u,'_blank')};if(/Firefox/.test(navigator.userAgent))setTimeout(a,0);%20else%20a();%20void(0);[/code]

こちらのコードであれば、Kindle本でもばっちり登録されます。

<a href="https://rashita.net/blog/?attachment_id=26125" rel="attachment wp-att-26125"><img src="https://rashita.net/blog/wp-content/uploads/2018/11/screenshot-43.png" alt="" width="686" height="497" class="alignnone size-full wp-image-26125" /></a>

Kindle本の登録が多い方はお使いください。

では、では。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01EL08HS6/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51JnodMK-LL._SL160_.jpg" alt="ソーシャル時代のハイブリッド読書術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01EL08HS6/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ソーシャル時代のハイブリッド読書術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.11.08</div></div><div class="amazlet-detail">C＆R研究所 (2016-04-21)<br />売り上げランキング: 107,915<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01EL08HS6/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
