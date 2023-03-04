---
title : Scrapboxの週間ページの補足
link : 28348
date : Mon, 20 May 2019 02:16:54 +0000
categories : ["scrapboxの用法","「タスク」の研究"]
tags : ["scrapbox"]
draft : false
author : 倉下忠憲
---

<a href="https://rashita.net/blog/?p=28337">クイック・レビュー</a>の補足です。

Scrapboxで作っている週間ページは、UserScriptを経由して以下のような日付リンクが自動的に作成されるようになっています。

<a href="https://rashita.net/blog/?attachment_id=28349" rel="attachment wp-att-28349"><img src="https://rashita.net/blog/wp-content/uploads/2019/05/screenshot-33.png" alt="" width="557" height="294" class="alignnone size-full wp-image-28349" /></a>

で、ここにその週コミットしたいプロジェクトとその指針を書いていくわけですが、そこで役立つのがリンク作成機能です。Scrapboxであれば、週間ページから移動することなく、プロジェクトページへのリンクが作れます。

一般的なツールだと、たぶん「プロジェクトリスト」（あるいはプロジェクトビュー）みたいなものをいったん開いてから、そこから情報を持ってくる必要があるわけですが、Scrapboxならその必要はありません。私の場合であればプロジェクトページの頭には&#x1f4d8;が入っているので、ブラケットにこれを入れて、何かそれっぽい言葉をいくつか入れれば、プロジェクトページへのリンクが作れます。

この「移動の手間がない」というのが、結構重要なのです。

でもって、このリンクを作る、ということすら若干手間に感じるときがあります。そこで関連ページです。

<a href="https://rashita.net/blog/?attachment_id=28350" rel="attachment wp-att-28350"><img src="https://rashita.net/blog/wp-content/uploads/2019/05/screenshot-34-700x437.png" alt="" width="700" height="437" class="alignnone size-large wp-image-28350" /></a>

ここには先週コミットしたプロジェクトがリストアップされています。プロジェクトとは継続的なものですから、だいたいはここからドラッグすれば、それで事足りちゃうわけです。でもって、この操作、若干バレットジャーナル的です。手書きで書き写しているわけではないですが、ドラッグ操作で取捨選択を行っています。

つまり、自動的にこのページに直接プロジェクトページへのリンクを追加されたくはないのです。だって、その週に続けてコミットするかどうかはわかりませんからね。もちろん、必要なければ消せばいいのですが、そうはいっても、そのような操作が必要であるという点で、私の「意志」が軽んじられているような印象があります。

その点、下に表示される関連ページから自分で選んでドラッグしてくる、というのならば、そこには選択があり、意志の介入の感覚があります。でもって、それほど手間でもありません。これがちょうどいい塩梅なのです。

ただし、単に先週の週間ページにプロジェクトページへのリンクがあるだけでは、次週の週間ページの関連にプロジェクトページが表示されることはありません（ややこしいので、下記画像参照）。ここに表示されるのは、「共通のリンクを持つページ」です。

<a href="https://rashita.net/blog/?attachment_id=28354" rel="attachment wp-att-28354"><img src="https://rashita.net/blog/wp-content/uploads/2019/05/87F380ED-3352-4035-8583-6FF2DA8396BF-700x933.jpg" alt="" width="700" height="933" class="alignnone size-large wp-image-28354" /></a>

つまり、各プロジェクトページの中に、先週の週間ページへのリンクがあり、また今週の週間ページにも先週の週間ページへのリンクがあればいいわけです。

後者については、もともとテンプレートに入れ込んであるのでこちらは問題ありません。

<a href="https://rashita.net/blog/?attachment_id=28351" rel="attachment wp-att-28351"><img src="https://rashita.net/blog/wp-content/uploads/2019/05/screenshot-35.png" alt="" width="570" height="193" class="alignnone size-full wp-image-28351" /></a>

では、各プロジェクトページは？　これも問題ありません。週間ページにプロジェクト名を記入し、そこに振り返りを書き込んだあとにAppend（New page機能の亜種）するからです。

※週間ページ
<a href="https://rashita.net/blog/?attachment_id=28352" rel="attachment wp-att-28352"><img src="https://rashita.net/blog/wp-content/uploads/2019/05/screenshot-36.png" alt="" width="568" height="207" class="alignnone size-full wp-image-28352" /></a>

※プロジェクトページ
<a href="https://rashita.net/blog/?attachment_id=28353" rel="attachment wp-att-28353"><img src="https://rashita.net/blog/wp-content/uploads/2019/05/screenshot-37-700x254.png" alt="" width="700" height="254" class="alignnone size-large wp-image-28353" /></a>

<a href="https://scrapbox.io/rashitamemo/%E3%83%97%E3%83%AD%E3%82%B8%E3%82%A7%E3%82%AF%E3%83%88%E3%83%9A%E3%83%BC%E3%82%B8%E3%81%AE%E8%BF%BD%E8%A8%98%E3%81%AB%E7%89%B9%E5%8C%96%E3%81%97%E3%81%9FNew_page%E3%81%AE%E3%82%A2%E3%83%AC%E3%83%B3%E3%82%B8UserScript">プロジェクトページの追記に特化したNew pageのアレンジUserScript - 倉下忠憲の発想工房</a>

逆に言いましょう。このようなAppendを行わない限り、来週の「関連するページ」にプロジェクトページが表示されることはありません。どれだけ週間ページにプロジェクトページへのリンクを貼っても、プロジェクトページに週間ページへのリンクが貼られない限りは、関連しないのです。つまり、コミットしていないプロジェクトは次週には表示されないことになります。この点が、地味に大きいです。

仮に週間ページにいろいろなプロジェクトを書いてしまっても、結局コミットする時間がなければそれはそのままスルーされることになり、一週間の振り返りでもAppendは発生しません。で、それがそのままそのプロジェクトへのコミット減少を引き起こすのです。つまり、「やらなければいけないリスト」の重圧が発生しません。間引かれていくのです。

もちろん、次週（やそれ以降）になって改めてそれにコミットしたいという気持ちが湧くならば、[&#x1f4d8; ]でリンクを作ればいいでしょう。先ほども書いたように、そのコスト自体はたいして大きいものではありません。手軽にできます。

以上のようなやり方をしている限り「長大なリストと毎回向き合う」みたいなことは避けられます。もちろん必要に応じてそうしたリストを参照することもありますが、あくまでそれは「必要に応じて」であって、毎度のことではありません。その辺が、気楽さ・気安さにつながっています。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51yMZ%2BQU40L._SL160_.jpg" alt="Scrapbox情報整理術" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Scrapbox情報整理術</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 19.05.20</div></div><div class="amazlet-detail">シーアンドアール研究所 (2018-08-16)<br />売り上げランキング: 12,092<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B07GJFBWWZ/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4065151562/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/31yz41bTULL._SL160_.jpg" alt="「やること地獄」を終わらせるタスク管理「超」入門 (星海社新書)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4065151562/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">「やること地獄」を終わらせるタスク管理「超」入門 (星海社新書)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 19.05.20</div></div><div class="amazlet-detail">倉下 忠憲 <br />講談社 <br />売り上げランキング: 18,389<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4065151562/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

