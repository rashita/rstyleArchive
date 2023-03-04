---
title : WorkFlowyの魔改造によりコラムの横並べが可能
link : 20114
date : Thu, 06 Apr 2017 02:29:50 +0000
categories : ["アウトライナーで遊ぼう","物書き生活と道具箱"]
tags : ["workflowy"]
draft : false
author : 倉下忠憲
---

WorkFlowyは便利で機能的なんですけども、やっぱり気になることがありますよね。

<a href="https://rashita.net/blog/?attachment_id=20115" rel="attachment wp-att-20115"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-500x275.png" alt="" width="500" height="275" class="alignnone size-medium wp-image-20115" /></a>

そうです。この右側の広大なスペース。これだったらヨーロッパ大陸から移民がやってきて開拓できるんじゃないかってくらいスペースが空いちゃってます。にも関わらず、縦一列で表示できる項目の数はそれほど多くないので、全体的な俯瞰性はおせじにも高いとは言えません。

これをなんとかしたい……。そう思う有志がこの世界にはいたわけです。そこからハリウッド的な感動ストーリーが始まるのかどうかはわかりませんが、いろいろやると、以下のように表示させられます。

<a href="https://rashita.net/blog/?attachment_id=20116" rel="attachment wp-att-20116"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-1-500x205.png" alt="" width="500" height="205" class="alignnone size-medium wp-image-20116" /></a>

oh! fantastic!

このトリッキーな表示に興味があるのならば、続きをご覧ください。

<h3>必要なアドオン</h3>

ブラウザはFirefoxを使っている前提で話を進めます。たぶんChromeさんでも似たように進められると思います。

まず必要なアドオンを揃えましょう。二つあります。

一つは、「Stylish」。webページに自分好みのCSSを当てられるアドオンです。もう一つは、「Tampermonkey」。こちらはwebページで自分好みのスクリプト(javascript）を走らせられるアドオンです。この二つを組み合わせて、コラムの横並べを実現します。

<a href="https://rashita.net/blog/?attachment_id=20119" rel="attachment wp-att-20119"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-4-500x28.png" alt="" width="500" height="28" class="alignnone size-medium wp-image-20119" /></a>

<a href="https://rashita.net/blog/?attachment_id=20120" rel="attachment wp-att-20120"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-5-500x35.png" alt="" width="500" height="35" class="alignnone size-medium wp-image-20120" /></a>

まずはこの二つをインストールしておきましょう。

<h3>Stylishの設定</h3>

次に、Stylishの設定に入ります。

WorkFlowyのページを開きながら、Stylishのアドオンボタンをクリックし、「このサイト用のスタイルを探す」をポチッと。

<a href="https://rashita.net/blog/?attachment_id=20118" rel="attachment wp-att-20118"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-3-500x337.png" alt="" width="500" height="337" class="alignnone size-medium wp-image-20118" /></a>

そこで表示されるページから「<a href="https://userstyles.org/styles/132660/workflowy-2-3-4-5-6-columns">WorkFlowy 2,3,4,5,6-columns!</a>」を探してください。まあ、わかりやすい名前ですね。で、それをインストール。

<a href="https://rashita.net/blog/?attachment_id=20117" rel="attachment wp-att-20117"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-2-500x161.png" alt="" width="500" height="161" class="alignnone size-medium wp-image-20117" /></a>

ついでにもう一つ、「WorkFlowy Total Minimalist」というstyleもインストールしておきましょう。WorkFlowy 2,3,4,5,6-columns!の解説ページにもリンクがありますが、ようは→のページです。 <a href="https://userstyles.org/styles/132659/workflowy-total-minimalist">https://userstyles.org/styles/132659/workflowy-total-minimalist</a> 

これで、Stylishの準備が整いました。ただし、これだけでは表示の仕方が設定されただけであり、アウトラインを動的に変更することはできません。それを担当するのが、Tampermonkeyです。

<h3>Tampermonkey</h3>

スクリプト、と聞いただけで情報免疫系が活発になって、目も耳も塞ぎたくなる方に朗報です。基本的にコピペだけでOKです。

まずは、以下のページにアクセス。

<a href="https://blog.workflowy.com/2016/05/19/different-fonts-for-different-workflowy-outlines/#more-1564">Different Fonts for Different WorkFlowy Outlines – WorkFlowy Blog</a>

何が行われているのかというと、特定のハッシュタグがついた項目のフォントを動的に変えちゃう、というシステムの紹介です。で、これをさらにハックして、コラムの横並べをしてやろうじゃないか、というのが、「WorkFlowy 2,3,4,5,6-columns!」のスタイルを作った人たちの意図なわけです。マッドな意図ですね。

で、そのページの中程にTampermonkeyの説明があり、「you can find here.」というリンクがあるので、そこからGithubのページにジャンプしてください。できれば、上のページもご覧頂きたいのですが、せっかちな方のために直リンクも。

<a href="https://gist.github.com/lukemt/bd90b41e9603e0737a30#file-workflowystylabletags_slim_version-js"> WorkflowyStylableTags_slim_version.js</a>

<a href="https://rashita.net/blog/?attachment_id=20121" rel="attachment wp-att-20121"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-6-500x237.png" alt="" width="500" height="237" class="alignnone size-medium wp-image-20121" /></a>

ここで、右上の「Raw」ボタンを押せば、コピペ可能なプレーンテキストが表示されるので、それを全文コピペ。あとは、そのコードを、Tampermonkeyに追加すればOKです。

Tampermonkeyのボタン（ブラウザの右上に表示されているやつです）を押して、「新規スクリプトを追加」を選択。

<a href="https://rashita.net/blog/?attachment_id=20129" rel="attachment wp-att-20129"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-13-500x249.png" alt="" width="500" height="249" class="alignnone size-medium wp-image-20129" /></a>

上のような画面が表示されると思うので、もともと書いてあるコードを消してから、先ほどコピーしてきたスクリプトを貼り付けます。

あとは、保存でOKです。クラウド時代の新生児にはわかりにくいかもしれませんが、保存ボタンはフロッピーディスクのアイコンです。フロッピーディスクとは、携帯用の固形食料で、というのはまったくの嘘ですが、エディタのメニューの左から二番目のアイコンです。

これで準備が整いました。

<h3>実際の運用</h3>

一度、WokrFlowyのページを開き直してください。それでTampermonkeyのスクリプトが適用されるはずです。

<a href="https://rashita.net/blog/?attachment_id=20122" rel="attachment wp-att-20122"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-7.png" alt="" width="226" height="93" class="alignnone size-full wp-image-20122" /></a>

上のように、「１」というマークが表示されていたら、１つのスクリプトが動いているよ、ということでOKサインです。さらにStylishで追加した二つのstyleが適用されていれば問題なし。こちらもStylishのボタンを押せば、適用されているスタイル名がチェックマーク付きで表示されるのですぐにわかります。

あとは、普通に項目を入力していき、横に並べたい（回り込みさせたい）項目の親の項目にハッシュタグをつけます。#cols-n というハッシュタグです。

<a href="https://rashita.net/blog/?attachment_id=20123" rel="attachment wp-att-20123"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-8-500x254.png" alt="" width="500" height="254" class="alignnone size-medium wp-image-20123" /></a>

<a href="https://rashita.net/blog/?attachment_id=20124" rel="attachment wp-att-20124"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-9-500x246.png" alt="" width="500" height="246" class="alignnone size-medium wp-image-20124" /></a>

<a href="https://rashita.net/blog/?attachment_id=20125" rel="attachment wp-att-20125"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-10-500x216.png" alt="" width="500" height="216" class="alignnone size-medium wp-image-20125" /></a>

<a href="https://rashita.net/blog/?attachment_id=20126" rel="attachment wp-att-20126"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-11-500x210.png" alt="" width="500" height="210" class="alignnone size-medium wp-image-20126" /></a>

<a href="https://rashita.net/blog/?attachment_id=20127" rel="attachment wp-att-20127"><img src="https://rashita.net/blog/wp-content/uploads/2017/04/screenshot-12-500x250.png" alt="" width="500" height="250" class="alignnone size-medium wp-image-20127" /></a>

#cols-6まで使えます。

<h3>さいごに</h3>

横に並べることで、圧倒的な俯瞰性を手にすることができ、「ああ、そうだ、我はこのUIを求めていたのだ」とご満悦な気分に浸れるのですが、こうしてしまうと、項目の移動に著しい制約がかかります。というか、コラム内の移動は自由なのですが、別のコラムへの移動は著しく困難です。というか、そのままの状態ではほぼ不可能といっていいでしょう。

まあ、これだけの魔改造をしているのですから、その程度の不便は甘受すべきです。もちろん、ハッシュタグを外せば、シュルリと元の一列に戻るので（これがなかなか軽快で楽しい）、その状態で移動させて、再びハッシュタグを付け戻す、というやり方はいつだって有効です。

上記を考慮すると、この横並べは作成の最中というよりも、アウトラインの移動がだいたい終わり全体をちょっと俯瞰してみたいな、とか、あるいはもう完成してしまって動かすことがないよ、という場合に使うのがFeel so goodなのでしょう。

ちなみに、私はこのシステムを非常に気に入っています。むしろこういうUIのアウトライナーが新しく来て欲しいくらいです。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51HoJpXhvnL._SL160_.jpg" alt="アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.04.06</div></div><div class="amazlet-detail">技術評論社 (2016-07-09)<br />売り上げランキング: 26,642<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51ymv5zS94L._SL160_.jpg" alt="クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.04.06</div></div><div class="amazlet-detail">インプレスR&D (2016-01-29)<br />売り上げランキング: 29,866<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>









