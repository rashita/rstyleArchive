---
title : Dynalistで項目リンクが簡単に作れるようになった
link : 26991
date : Tue, 05 Mar 2019 01:57:15 +0000
categories : ["0-知的生産の技術"]
tags : ["dynalist","機能紹介"]
draft : false
author : 倉下忠憲
---

Dynalistの最近のアップデートが衝撃でした。

<a href="https://blog.dynalist.io/2019-february-update/">February update</a>

<blockquote>
“[[” link suggestion dialog now prioritizes results from the same document.
</blockquote>

開きブラケットを二つ重ねると、同じドキュメントにある別の項目のリンクを提案してくれるダイアログが表示されます。

<a href="https://gyazo.com/d4a9fb758fdcfd36077cf77346ec5a96"><video alt="Video from Gyazo" width="696" autoplay muted loop playsinline controls><source src="https://i.gyazo.com/d4a9fb758fdcfd36077cf77346ec5a96.mp4" type="video/mp4" /></video></a>

これにより、いちいち項目を閉じ開きして別項目を探すことなく、項目リンクが作れるようになりました。

動作については、二重開きブラケットの直後に入力した文字列が含まれている項目を探しているっぽいです。スペースを使っての二つ以上のキーワードの絞り込み、みたいなことはできないので、一つの文字列として入力するのが吉です。

また、以下のような性質があります（アップデートがあれば変わるかもしれません）。

・小文字と大文字は区別しない

・[[Scrapboxと入力した場合、飛び飛びでもその順番でこの文字列が出てくる項目もヒットする

<a href="https://rashita.net/blog/?attachment_id=26993" rel="attachment wp-att-26993"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-1-700x458.png" alt="" width="700" height="458" class="alignnone size-large wp-image-26993" /></a>

・曖昧な検索は許容されない

<a href="https://rashita.net/blog/?attachment_id=26994" rel="attachment wp-att-26994"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-2-700x518.png" alt="" width="700" height="518" class="alignnone size-large wp-image-26994" /></a>

<a href="https://rashita.net/blog/?attachment_id=26995" rel="attachment wp-att-26995"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-3-700x512.png" alt="" width="700" height="512" class="alignnone size-large wp-image-26995" /></a>

<a href="https://rashita.net/blog/?attachment_id=26996" rel="attachment wp-att-26996"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-4-700x554.png" alt="" width="700" height="554" class="alignnone size-large wp-image-26996" /></a>

<a href="https://rashita.net/blog/?attachment_id=26997" rel="attachment wp-att-26997"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-5-700x546.png" alt="" width="700" height="546" class="alignnone size-large wp-image-26997" /></a>

上記のように、文字列が出てくる順番が適正でないと検索結果に項目が出てきません。この点が、若干の使いにくさではあります。「たしか、出版社とウェブというキーワードが入ってたんだけど……」みたいな思い出し方をしたときに、順番を入れ換えて探す必要がありますし、二つ以上になると相当厄介です。

この点、Scrapboxだと柔軟です。

<a href="https://rashita.net/blog/?attachment_id=26998" rel="attachment wp-att-26998"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-6.png" alt="" width="505" height="282" class="alignnone size-full wp-image-26998" /></a>

<a href="https://rashita.net/blog/?attachment_id=26999" rel="attachment wp-att-26999"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-7.png" alt="" width="447" height="229" class="alignnone size-large wp-image-26999" /></a>

・タグの中身も検索対象となる

<a href="https://rashita.net/blog/?attachment_id=27000" rel="attachment wp-att-27000"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-8-700x253.png" alt="" width="700" height="253" class="alignnone size-large wp-image-27000" /></a>

・項目リンクも検索対象となる

<a href="https://rashita.net/blog/?attachment_id=27001" rel="attachment wp-att-27001"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-9-700x306.png" alt="" width="700" height="306" class="alignnone size-large wp-image-27001" /></a>

・被リンク先はわからない

（むしろこれがわかるScrapboxがすごい、という噂はあります）


<h2>さいごに</h2>

というわけで、はっきりとその項目の存在が分かっていて、そこへのリンクを作りたい、というときなんかには便利そうです。

たとえば買った本の記録を残しているとして、日記を付けているときに、その本の項目へのリンクを作る、なんてシチュエーションではこの機能は最高でしょう。

逆に、アイデアのようにちょっと曖昧なものを引き出すときには結構苦労するかもしれません。

あと、作ったリンクも検索対象となるので、何度も参照される人気項目だと検索結果が項目リンクで埋まってしまう可能性もあります。これはまあ、使い方次第でしょう。

もう一つ、二重ブラケットの後に入力した文字列は順番に、しかし飛び飛びでもOKという形なので、ネーミングに規則性を持たせておけば、ある程度の絞り込みをかけることができます。

たとえば、書籍のタイトルは必ず『』で括り、その後ろに著者名を入力しておく、という規則があれば、

まず『で書籍リストが表示されますし、

<a href="https://rashita.net/blog/?attachment_id=27002" rel="attachment wp-att-27002"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-10-700x514.png" alt="" width="700" height="514" class="alignnone size-large wp-image-27002" /></a>

その後にタイトルに含まれる文字列を入れれば絞り込みができます。

<a href="https://rashita.net/blog/?attachment_id=27003" rel="attachment wp-att-27003"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-11.png" alt="" width="613" height="252" class="alignnone size-full wp-image-27003" /></a>

あるいは、著者名を続けることで絞り込むことも可能です。

<a href="https://rashita.net/blog/?attachment_id=27004" rel="attachment wp-att-27004"><img src="https://rashita.net/blog/wp-content/uploads/2019/03/screenshot-12.png" alt="" width="610" height="294" class="alignnone size-large wp-image-27004" /></a>

こういう使い方はなかなか良さそうですね。

ちょうど、<a href="https://scrapbox.io/rashitamemo/Evernote%E3%81%A7%E3%82%82%E7%B0%A1%E5%8D%98%E3%81%AB%E3%83%8E%E3%83%BC%E3%83%88%E3%83%AA%E3%83%B3%E3%82%AF%E3%82%92%E8%BF%BD%E5%8A%A0%E3%81%97%E3%81%9F%E3%81%84">Evernoteでも同じような機能をAppleScriptで実装</a>して使っていたところなので、Dynalistのこのアップデートは「わかってるじゃん」という感じで嬉しくなりました。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 19.03.05</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 43,077<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
