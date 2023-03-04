---
title : MacのEvernoteで、ノートの見出しマークダウンをhタグに変換するスクリプト
link : 19001
date : Fri, 23 Sep 2016 01:44:27 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

Evernoteのノートエディタは、リッチテキストを扱えるのですが、ワープロアプリのような見出しの設定ができません。

かといって、いちいち文字サイズを大きくして、太字に設定して、みたいなのは面倒なわけです。

そういうとき、たとえばUlyssesでマークダウン式で書き、Evernoteにエクスポートすればうまい具合に見出しが整った文章が作成できるわけですが、同じことがEvernote単独で完結すればそれはもう素晴らしいわけです。

というわけで、簡単なスクリプトを書きました。

<h3>サンプル</h3>

<a href="https://rashita.net/blog/?attachment_id=19002" rel="attachment wp-att-19002"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot33-500x207.png" alt="screenshot" width="500" height="207" class="alignnone size-medium wp-image-19002" /></a>

このように書いた後、スクリプトを走らせると、以下のようになります。

<a href="https://rashita.net/blog/?attachment_id=19003" rel="attachment wp-att-19003"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot34-500x277.png" alt="screenshot" width="500" height="277" class="alignnone size-medium wp-image-19003" /></a>

完璧です。

ちなみに、変換は不可逆で後戻りできませんので、その点にはご注意を。

<h3>スクリプトの中味</h3>

ちなみに、このスクリプトで変換できるのは、見出しだけです。#〜######の6段階の見出し。その他のマークダウンはまったくサポートされておりませんので、「おい、中途半端だな」と思われる方はご自分で実装してくださいませ。

<script src="https://gist.github.com/rashita/e2c45d2b7fecdec19f127d9b25de5163.js"></script>

<h3>苦労点</h3>

当初は、「ようするに正規表現で#のついている行を見つけて、置換すればいいんだろう」ぐらいに考えていました。ある部分まではそれで正解ですが、ややこしいのはEvernoteのノートの内部構造です。

通常のマークダウンの処理では、「行頭に#があるものを見つける」的な動きになるのでしょうが、Evernoteではそれがうまくいきません。何でだろうな、と思っていたら、そういえばEvernoteのノートの取得は、HTMLなのでした。どういうことかというと、各行がDivダグで囲われているのです。だから、行頭に#がないのです。

だったら、プレーンテキストで取得すればいいんじゃないか、となりますが、書き込みたい要素がHTML（hタグ）なので、これではうまくいきません。

なので発想を切り替えて、「Divの開きタグ+#」という検索条件にしました。今のところ、これで問題なく動いております。

<h3>さいごに</h3>

Evernoteのノートエディタで直接文章を書いている方は少ないかもしれませんが、もしバリバリ使っているなら一度試してみて下さい。わりと便利です。

<ol>
<li>スクリプトエディタを立ち上げて、上記のコードをコピペ</li>
<li>名前を付けて保存</li>
<li>スクリプトエディタの「環境設定」で、「メニューバーにスクリプトメニューを表示」をチェック</li>
<li>スクリプトメニューから、スクリプト用のフォルダが表示</li>
<li>そこに先ほどのスクリプトを保存する</li>
</ol>

<a href="https://rashita.net/blog/?attachment_id=19004" rel="attachment wp-att-19004"><img src="https://rashita.net/blog/wp-content/uploads/2016/09/screenshot35.png" alt="screenshot" width="479" height="349" class="alignnone size-full wp-image-19004" /></a>

これで、メニューバーからいつでもこのスクリプトを起動できます。Evernote用のスクリプトフォルダに入れておけば、Evernoteがアクティブになっているときしか表示されないので、それはそれで便利です。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.09.23</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 607<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/515rWUhPqbL._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.09.23</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 35,707<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>




