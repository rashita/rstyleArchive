---
title : WorkFlowyの左部分に特定項目のindexを表示
link : 22733
date : Tue, 22 Aug 2017 03:33:31 +0000
categories : ["アウトライナーで遊ぼう"]
tags : ["javascript","tamparmonkey","workflowy"]
draft : false
author : 倉下忠憲
---

WorkFlowyの左側のスペースって、何かに使いたいですよね。

<a href="https://rashita.net/blog/?attachment_id=22734" rel="attachment wp-att-22734"><img src="https://rashita.net/blog/wp-content/uploads/2017/08/screenshot-16-500x306.png" alt="" width="500" height="306" class="alignnone size-medium wp-image-22734" /></a>

自分のこれまでのアウトライナー体験から言うと、ここに何かしらのindexがあれば使い勝手が良さそうです。

特にこのincubator項目は縦に長くなっているので一覧性が悪く、しかもそうした項目の中に特別な奴ら（大きなアイデアの核となるような項目）がいくつか存在しているので、そうしたものだけをピックアップしたindexを作れば、「今の自分が抱えているアイデア核の一覧」が作れるんじゃないか。そんなことを思い浮かべました。

幸いブラウザ拡張のTamparmonkeyを使えば、自分が書いたJavaScriptを割り込ませることができます。うまくやれば、実現可能でしょう。

<h2>アイデアのネタもと</h2>

とは言え、いきなりこういう欲求が出てきたわけではありません。以前、以下のスクリプトを覗いていた経験があったからです。

<a href="https://note.mu/maro_draft/n/n6487afd187c0">WorkFlowyの文字数カウントブックマークレット | マロ。 | note</a>

上記はWorkFlowyのテキスト文字数をカウントしてくれるだけなく、それを左部分に埋め込んで表示してくれるという大変ありがたい機能です。で、上記のコードをデコードして自分なりに読んでいて、「WorkFlowyのテキスト全体を扱うこと」「その結果を受けてページに要素を追加すること」ができるんだな、ということ感覚的に理解していました。

あとは、この「WorkFlowyのテキスト全体を扱うこと」を、文字数カウントではなく、一定の検索条件による要素の抽出にすれば、私が望む機能は実装できそうです。

<h2>欠けたパーツ</h2>

あと必要だったのは、第一にWorkFlowyの全文から特定の条件に合う要素だけを検索する方法。さらに、それぞれの項目はリンクになっていないと意味がないので、項目のリンクを取り出す方法も必要です。逆に言えば、この二つさえわかれば、あとは何とかなるでしょう。

で、探索していくと、ばっちり見つけられてしまうのがインターネットワールドです。

<a href="https://note.mu/maro_draft/n/n05629502bb41?creator_urlname=maro_draft">WorkFlowyで文字列置換を行うブックマークレット　ReplaceFlowy | マロ。 | note</a>

<a href="https://note.mu/maro_draft/n/n801215fbf65e?creator_urlname=maro_draft">WorkFlowyの目次リストをつくるbookmarklet | マロ。 | note</a>

マロ。さんには頭があがりません。特に後者が参考になりました。いや、参考になったというか、このスクリプトで出力される形式をちょこっと変更すれば、ほぼ望みのものが手に入ります。もともとのスクリプトは、'[項目名] URL'の形になっていますが、それをAタグを使って囲む形にすればバッチリです。あとは、表示する項目を頭に特定の文字が付いたものだけにすれば、完璧でしょう。

これは最近覚えた正規表現の^を使えば、ばっりちそうです。

で、その（日曜大工感溢れる）コードをここで公開しようかと思ったのですが、はるかにスマートなコードをまるみ(<a href="https://twitter.com/marumi_app">@marumi_app</a>)さんが書いてくださりました。

<a href="https://marumi.nap.jp/blog/post/2017/0821-workflowy_leftpanel/">WorkFlowyの項目を抽出して、左に表示する</a>

さすが、MemoFlowyやHandyFlowyの開発者さんです。

<div class="sticky-itslink"><a href="https://itunes.apple.com/jp/app/memoflowy/id1052582668?mt=8&uo=4&at=11l4y8" rel="nofollow" target="_blank"><img src="http://is1.mzstatic.com/image/thumb/Purple122/v4/c9/d3/a0/c9d3a099-5861-6ffb-09d3-574bce05ca6a/source/60x60bb.jpg" style="border-style:none;float:left;margin:5px;" alt="MemoFlowy" title="MemoFlowy" ></a><div class="sticky-itslinktext"><a href="https://itunes.apple.com/jp/app/memoflowy/id1052582668?mt=8&uo=4&at=11l4y8" rel="nofollow" target="_blank">MemoFlowy</a><br>Michinari YAMAMOTO<br>価格： 0円<br><span style="font-size:xx-small;">posted with <a href="http://sticky.linclip.com/linkmaker/" target="_blank">sticky</a> on 2017.8.22</span></div><br style="clear:left;" ></div> 

<div class="sticky-itslink"><a href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&uo=4&at=11l4y8" rel="nofollow" target="_blank"><img src="http://is5.mzstatic.com/image/thumb/Purple117/v4/92/b6/df/92b6df7b-04a9-4f56-da13-59503d81691d/source/60x60bb.jpg" style="border-style:none;float:left;margin:5px;" alt="HandyFlowy" title="HandyFlowy" ></a><div class="sticky-itslinktext"><a href="https://itunes.apple.com/jp/app/handyflowy/id1080279196?mt=8&uo=4&at=11l4y8" rel="nofollow" target="_blank">HandyFlowy</a><br>Michinari YAMAMOTO<br>価格： 0円<br><span style="font-size:xx-small;">posted with <a href="http://sticky.linclip.com/linkmaker/" target="_blank">sticky</a> on 2017.8.22</span></div><br style="clear:left;" ></div> 

あとは、そのスクリプトを何かしらのトリガーによって発動すればOKで、私はショートカットキーを選択しました。これもJavaScriptで書けます。

たとえば、こんな感じ

[javascript]
document.onkeydown = function(e) {
    var keyCode = false;
    if (e) event = e;
    if (event) {
        if (event.keyCode) {
            keyCode = event.keyCode;
        } else if (event.which) {
            keyCode = event.which;
        }
    }
    if (keyCode === 71 &amp;　event.shiftKey === true) {

        if(e.preventDefault){
			// デフォルトの動作を無効化する
			e.preventDefault();
		}else{
			// デフォルトの動作を無効化する（非標準）
			return false;
		}

        indexMaker();// 発動させたいファンクション

       }
};
[/javascript]

これで、shift+gで、インデックスが作成されます。

その動作を動画でも確認してみましょう。

<iframe width="560" height="315" src="https://www.youtube.com/embed/wdLeuBXjKoA" frameborder="0" allowfullscreen></iframe>

いやはや、我ながらマニアックですね。

さらにこのindex領域にボタンを付けて、別の抽出条件の結果や、メタ情報の表示を切り替えられるようにすれば、もはやまったく別のツールに生まれ変わるのでは、という予感もしていますが、そんなことをしている間にどんどん原稿を書く時間が削られていくので、カスタマイズはほどほどにしておきましょう。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51HoJpXhvnL._SL160_.jpg" alt="アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.22</div></div><div class="amazlet-detail">技術評論社 (2016-07-09)<br />売り上げランキング: 32,060<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51ymv5zS94L._SL160_.jpg" alt="クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.08.22</div></div><div class="amazlet-detail">インプレスR&D (2016-01-29)<br />売り上げランキング: 37,336<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

