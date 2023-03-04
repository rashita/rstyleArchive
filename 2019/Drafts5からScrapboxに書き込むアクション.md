---
title : Drafts5からScrapboxに書き込むアクション
link : 28434
date : Fri, 31 May 2019 02:20:51 +0000
categories : ["scrapboxの用法"]
tags : ["drafts","scrapbox"]
draft : false
author : 倉下忠憲
---

<blockquote class="twitter-tweet" data-cards="hidden" data-lang="ja"><p lang="ja" dir="ltr">[ゆるぼ]Drafts5からScrapboxの特定のページにテキストを追記できるアクションの作り方。javaが使えるのでtextwellと同じ手法でいけるはずなのですが・・・<a href="https://t.co/c7SQZMRTBF">https://t.co/c7SQZMRTBF</a></p>&mdash; るう (@ruu_embo) <a href="https://twitter.com/ruu_embo/status/1133519178713915394?ref_src=twsrc%5Etfw">2019年5月28日</a></blockquote>
<script async src="https://platform.twitter.com/widgets.js" charset="utf-8"></script>

よし、じゃあ、書いてみますか。

経過は以下。

<a href="https://scrapbox.io/thinkandcreateteck/Drafts5%E3%81%8B%E3%82%89Scrapbox%E3%81%AB%E8%BF%BD%E8%A8%98%E3%81%99%E3%82%8BAction#5cef37b39dc7d80000a55aba">Drafts5からScrapboxに追記するAction - 考えて、生み出す技術(TAC）</a>

まず、無料ユーザーの場合はアクションのカスタマイズができないっぽいので、以下の神アクションを導入。

<a href="https://wineroses.hatenadiary.org/entry/20180422/p1">Drafts5で作ろう、自作アクション入門(1) - W&R : Jazzと読書の日々</a>

上のページにある「ActionMaker」を登録するところまでが下準備。これでDraft5に書いたコードをアクションとして登録できるようになります。一行目がタイトルとして使用されるので注意してください。

で、実際のコード。たとえば「<a href="https://scrapbox.io/rashitamemo/%E3%80%8C%E3%81%A9%E3%81%86%E3%81%9B%E8%A8%98%E4%BA%8B%E3%81%AB%E3%81%97%E3%81%8D%E3%82%8C%E3%81%AA%E3%81%84%E3%83%A1%E3%83%A2%E3%81%9F%E3%81%A1%E3%80%8D%E3%81%AE%E4%BE%9B%E9%A4%8A%E7%A5%AD">「どうせ記事にしきれないメモたち」の供養祭 - 倉下忠憲の発想工房</a>」に追記する場合は以下のようになります。

[code]goScrapbox
text = editor.getText();
const homeUrl = 'https://scrapbox.io/rashitamemo/%E3%80%8C%E3%81%A9%E3%81%86%E3%81%9B%E8%A8%98%E4%BA%8B%E3%81%AB%E3%81%97%E3%81%8D%E3%82%8C%E3%81%AA%E3%81%84%E3%83%A1%E3%83%A2%E3%81%9F%E3%81%A1%E3%80%8D%E3%81%AE%E4%BE%9B%E9%A4%8A%E7%A5%AD';
url = homeUrl +&quot;?body=&quot; + encodeURIComponent(text);
app.openURL(url);
editor.focus();
[/code]

なので、homeUrlのところに、ご自分の追記したいページのURLをぶっこんでもらえればOKです。あと、最初のhttps:の部分をsbporter:に差し替えると、SafariではなくPorter for Scrapboxで開くので、その辺はお好みで。

で、上記だと「あらかじめ指定してあるページに追記」しかできないので、少し動作を増やしたバージョンも。

[code]
goScrapbox
//プロジェクトのURLを設定。
//https:をsbporter:にすればPorter for Scrapboxでひらきます
const homeUrl = 'https://scrapbox.io/rashitamemo/';
//本文に追記したい要素を（ex.[drafts],\n[drafts] 。必要なければこのままで
const tag = &quot;&quot;;
const itemList = [];
itemList.push('「どうせ記事にしきれないメモたち」の供養祭');//追記したい固定ページのタイトルを入力する
itemList.push('新規');//一行目をタイトルにしてページを作る
itemList.push('日記');//その日の日記ページに追記（存在なければ新規作成）
p = Prompt.create();
p.title = &quot;？&quot;;
for(i=0; i &lt; itemList.length; i++) p.addButton(itemList[i]);
p.show();
s = p.buttonPressed;
const now = new Date();
const year = now.getFullYear();
const month = now.getMonth()+1;
const date = now.getDate();
const dateT = [&quot;日&quot;,&quot;月&quot;,&quot;火&quot;,&quot;水&quot;,&quot;木&quot;,&quot;金&quot;,&quot;土&quot;];
const day = dateT[now.getDay()];
const hours = now.getHours();
const minutes = now.getMinutes();
const seconds = now.getSeconds();
text = editor.getText();
lines = text.split(/\r\n|\r|\n/);
if (s == itemList[0]){
url = homeUrl + encodeURIComponent(s) + &quot;?body=&quot; + encodeURIComponent(text);
}else if (s == itemList[1]){
title = lines[0] == &quot;&quot; ? &quot;無題ノート&quot; : lines[0].trim()
url = homeUrl + encodeURIComponent(title) + &quot;?body=&quot; + encodeURIComponent(text + tag);
}else if (s == itemList[2]){
diaryTitle = year + &quot;/&quot; +  month + &quot;/&quot; +  date;
url = homeUrl + encodeURIComponent(diaryTitle) + &quot;?body=&quot; + encodeURIComponent(text + tag) ;
}
app.openURL(url);
editor.focus();
[/code]

これで三種類の動作から選択できます。

<a href="https://rashita.net/blog/?attachment_id=28436" rel="attachment wp-att-28436"><img src="https://rashita.net/blog/wp-content/uploads/2019/05/F4726F99-D361-4501-B6D8-47402937FECB.jpg" alt="" width="640" height="1136" class="alignnone size-full wp-image-28436" /></a>

上から、「指定してあるページへのつき」「一行目をタイトルにして新規ページの作成」「その日の日付をタイトルにしたページを作成」の三種類です。日付のタイトルについては、 下の方に出てくる diaryTitle = year + "/" +  month + "/" +  date; のところをいじってもらえば間の記号やらなんやらは変更できます。

というわけで、おおむね機能するアクションが書けたわけですが、「書き込みが終わったら、Drafts5に戻ってくる」という動作の指定方法がぜんぜんわかりませんでした。なにせアクションを書いたのはこれが初めてなのです。

なんとか、x-success というキーワードには辿り着きましたが、そこで力尽きました。

まあ、左上からDrafts5に戻れますので、とりあえずはそれで良しとしておきましょう。

<strong>▼こんなやりかたも：</strong>

<a href="http://sorashima.hatenablog.com/entry/Drafts5Append2ScrapboxNonProgramming">Drafts 5からScrapboxの特定のページに追記 ノンプログラミング版 - #ToDo 関連のメモ ( #sorashima )</a>

<strong>▼こんな一冊も:</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 19.05.31</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 68,823<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
