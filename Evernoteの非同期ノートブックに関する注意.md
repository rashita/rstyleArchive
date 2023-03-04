---
title : Evernoteの非同期ノートブックに関する注意
link : 18826
date : Wed, 24 Aug 2016 01:55:52 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

Evernoteには同期ノートブックと、ローカルノートブックの二種類があります。

同期ノートブックは、クラウド上のサーバーに内容をアップロードすることで、その中身を他の端末のEvernoteと同期してくれます。対して、ローカルノートブックは、どこにも内容がアップロードされない代わりに、中身を参照できるのはその端末だけです。

ノートの中身によっては、サーバーにアップするのはちょっと……みたいなこともあるでしょうから、そうしたノートはローカルノートブックに置いておけばよいでしょう。

ただし、このノートブックの扱いには、ちょっと注意が必要です。

<h3>ノートの移動ではない</h3>

最初に結論だけ書くと、ノートリンクが特殊になります。

何かノートを作ったとしましょう。そのノートはinbox（デフォルトのノートブック）に作成されますし、それはつまり同期ノートブックということです。

<a href="https://rashita.net/blog/?attachment_id=18827" rel="attachment wp-att-18827"><img src="https://rashita.net/blog/wp-content/uploads/2016/08/screenshot29-500x157.png" alt="screenshot" width="500" height="157" class="alignnone size-medium wp-image-18827" /></a>

そうして作成したノートを、ローカルノートブックに移動させます。すると、不思議な変化が。ゴミ箱にも同じノートが生まれているのです。

<a href="https://rashita.net/blog/?attachment_id=18828" rel="attachment wp-att-18828"><img src="https://rashita.net/blog/wp-content/uploads/2016/08/screenshot30-500x162.png" alt="screenshot" width="500" height="162" class="alignnone size-medium wp-image-18828" /></a>

<a href="https://rashita.net/blog/?attachment_id=18829" rel="attachment wp-att-18829"><img src="https://rashita.net/blog/wp-content/uploads/2016/08/screenshot31-500x155.png" alt="screenshot" width="500" height="155" class="alignnone size-medium wp-image-18829" /></a>

考えてみればこれは当たり前で、ローカルノートブックに置かれるということは、同期ノートブックからは取り除かれることを意味します。同期ノートブック同士の移動であれば、単にデータベースの「notebook」の値を書き換えれば済む話ですが、非同期への移動となると、削除が必要になってくるわけです。

つまり、同期ノートブックにあったノートと、ローカルノートブックに移動されたノートは「別物」だということです。中身はまったく同じですが、そのノートはコピーされてできたものなのです。

中身が同じなので困ることはほとんどありませんが、唯一の例外がノートリンクです。ノートリンクはノートの固有のアドレスを参照するので、ノートが変われば、その値も変わります。つまり、同期ノートブックに置かれているときに取得したノートリンクは、そのノートをローカルノートブックに移動させたときに、機能不全を起こすのです。

<a href="https://rashita.net/blog/?attachment_id=18830" rel="attachment wp-att-18830"><img src="https://rashita.net/blog/wp-content/uploads/2016/08/screenshot32-500x405.png" alt="screenshot" width="500" height="405" class="alignnone size-medium wp-image-18830" /></a>

この機能不全は、ノートをローカルノートブックから同期ノートブックに戻しても変わりません。なにせローカルノートブックにあるノートは、もう別のノートなのです。もし、ノートリンクの機能不全を解消したければ、ローカルノートブックからではなく、ゴミ箱から復元してください。それでばっちりです。

では、逆向きの動きはどうでしょうか。

ローカルノートブックに置かれているときに取得したノートリンクは、そのノートを同期ノートブックに移したときにどうなるか？

これは問題ありません。なぜならローカルノートブックから同期ノートブックへの移動はノートの削除＆コピーを伴わないからです。単に、そのノートが同期リストに追加されるだけなんですね。こちらはノートは「同じもの」なのでノートリンクもそのままです。

<h3>さいごに</h3>

ローカルノートブックの使用比率も、ノートリンクの使用比率もそれほど高くはないと思いますが、もし多用されているならばご注意ください。私は50ほどのノートをうっかりローカルノートブックに移してしまい、ノートリンクが一斉に死んでしまったのでかなり慌てました。

そういうときはゴミ箱をチェックです。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.08.24</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 1,195<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="http://ecx.images-amazon.com/images/I/515rWUhPqbL._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 16.08.24</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 273,937<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>






