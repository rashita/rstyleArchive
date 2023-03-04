---
title : Twitterのbotを作る２つの方法
link : 3158
date : Wed, 06 Jan 2010 04:12:39 +0000
categories : ["物書き生活と道具箱"]
tags : ["twittbot","twitter"]
draft : false
author : 倉下忠憲
---

最近、Twitterのbotシステムにちょっと興味が出てきたのでいろいろ下調べしました。

基本的にbotを運用するためには二つの方法があるようです。

<!--more-->

Twitterで定期的につぶやいたり、ある発言に反応したり、リプライに対して返信したり、といったことを「自動的」に行うのがbotです。基本的に専用のアカウントで作られています。代表例を挙げればきりがありません。アニメキャラの発言や、名言を集めたもの、株価などをつぶやくbotなど数限りなくあります。

「自動」で行う、というのはTwitterが提供しているAPIを利用して、プログラム上からつぶやきを流すということになります。
定期的に情報を更新しておきたいものや、ネタ的なものまで用途はいろいろあるでしょう。

さて、その作り方ですが、とりあえずbot用のTwitterアカウントを取るところから始めましょう。それが出来た方は以下の二つの方法から選択できます。

<strong>１　サーバーにbotプログラムを置く
２　botを提供しているサービスを使う</strong>

です。

<h3>１　サーバーにbotプログラムを置く</h3>
　この場合、当然自前のサーバーかレンタルサーバーを持っている必要があります。
　botプログラムは別になんでもよいのですが、調べて見るとPHPで書いたものが多いようです。普通のプログラミング言語をさわったことがある方ならばPHPのbotプログラム自身はそれほど難しい物ではないようです。

　基本的な動作をするプログラムも公開されているようでそれを改変して使うこともできそうです。

　しかしながら、ややギークよりな方法になりますので、今回はこの方法の詳細については割愛します。気になる方は以下の私の下書きメモにあるリンクをたどってもらえばある程度理解できることでしょう。
<a href="http://r-style.posterous.com/twitter-bot">Twitter botに関する情報集め</a>

<h3>２　botを提供しているサービスを使う</h3>
　その名も「twitter bot GENERATOR」というサービスがあります。テスト公開が2009-12-21 となっているので比較的若いサービスですね。

　bot専用のアカウントを取って、以下のページからログインするだけ。簡単です。
<a href="http://twittbot.net/">http://twittbot.net/</a>

<div class="kwout" style="text-align: center;"><img src="http://kwout.com/cutout/a/s4/fb/qs2_bor_rou_w350.jpg" alt="http://twittbot.net/" title="twitter ボットジェネレーター - 簡単にbotを作成" width="350" height="183" style="border: none;" usemap="#map_as4fbqs2" /><map id="map_as4fbqs2" name="map_as4fbqs2"><area coords="44,0,116,1" href="http://twittbot.net/modules/bot/index.php?page=bot_list" alt="" shape="rect" /><area coords="55,48,75,57" href="http://twitter.com/" alt="" shape="rect" /><area coords="0,0,43,1" href="http://twittbot.net/" alt="" shape="rect" /></map><p style="margin-top: 10px; text-align: center;"><a href="http://twittbot.net/">twitter ボットジェネレーター - 簡単にbotを作成</a> via <a href="http://kwout.com/quote/as4fbqs2">kwout</a></p></div>

拍子抜けするほど簡単に登録できます。

つぶやきの登録もテキストエリアに入力していくだけです。詳細設定で登録順につぶやくか、ランダムにつぶやくかも選べます。

返信機能やランダム返信の機能もあります。あと、時刻を指定してのつぶやきもでき、曜日の設定もできます。必要な機能はほぼそろっていると言っても過言ではないでしょう。

プログラミングの知識はまったくいりません。ただつぶやきたいワードを登録していくだけ。簡単きわまりないですね。現在（2010年1月6日）2229のボットがここから生まれているようです。


というわけで、私も<a href="http://twitter.com/toikake_bot">toikake_bot</a>なるものを作りました。ランダムに質問を投げかけてくるbotです。今のところ2時間毎のつぶやきと、朝7時頃と夜8時頃それぞれに特定のつぶやきがあります。
※現在リプレイされても何も反応を示しません。

名前の通り質問というよりは「問いかけ」に近いものです。本質に迫る問いかけ、哲学的な問いかけを充実させていく予定です。よければフォローしてやって下さい。

<a href="http://twitter.com/toikake_bot">toikake_bot</a>by Rashita

<div class="column">
編集後記：
久々にPHPでプログラム書こうかと思っていたら、ものすごい簡単で便利なサービスがありました。定期的に何かを告知したり、遊び心のbotを作ったりと用途と可能性はさまざまあると思います。面白いbot作ったら、教えて下さいませ。</div>