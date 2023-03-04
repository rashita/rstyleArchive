---
title : CotEditorのアウトラインメニューを使う
link : 14847
date : Mon, 17 Nov 2014 02:08:03 +0000
categories : ["物書き生活と道具箱"]
tags : ["coteditor"]
draft : false
author : 倉下忠憲
---

プレーンな文章を書くときには「<a href="http://coteditor.com/" target="_blank">CotEditor</a>」を使っています。

で、このCotEditorの「アウトラインメニュー」がなかなか便利なのです。ボリュームある文章を書く際に、大きな効果を発揮してくれます。

プログラマの方ならお馴染みでしょうが、文章書きの方は「なにそれ？」かもしれないので簡単に紹介しておきましょう。

<H3>What's アウトラインメニュー？</H3>

そもそも「アウトラインメニュー」とは何かというと、アウトラインのメニューです。

こういう文章があるとしましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot16.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot16-1024x837.png" alt="screenshot" width="500" height="" class="alignnone size-large wp-image-14848" /></a>

ちょっと寄ってみます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot17.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot17.png" alt="screenshot" width="407" height="212" class="alignnone size-full wp-image-14849" /></a>

文章の上の方に、見出しに対応するメニューが出ていますね。これがアウトラインメニューです。ぽちっとクリックしてみると、

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot18.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot18.png" alt="screenshot" width="390" height="140" class="alignnone size-full wp-image-14850" /></a>

こういう風に表示され、どれかを選択すれば文章中のその部分にジャンプする、というわけです。ようするに目次的に機能してくれるんですね。私のメルマガは1万字を余裕でオーバーするので、こういうジャンプ機能はたいへんありがたいものです。

<H3>ルールを設定する</H3>

もちろん、文章を書いている途中で「よし、ここに目次の項目を設定しよう」なんて細かい作業をちまちまやる必要はありません。あるルールに基づいて文を書けば、自動的にエディタがアウトラインを認識してくれます。

サンプルで挙げた文章で言えば、文頭の「○」がそのルールです。文の頭に○を一つ置いておけば、さっきのようなアウトラインメニューが自動で作成されるわけです。

で、そのルールなんですが、もとから設定されているものを利用することもできますし、独自で作成することも可能です。私が使っているのは独自ルールの方。で、どうやってそれを設定するのかなんですが、まずはメニューから「環境設定」を開き、「フォーマット」の項目を表示させましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot19.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot19.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14851" /></a>

で、適当なスタイルを選んで、編集ボタン（ペンのアイコン）を押します。試しに標準で準備されているHTMLのスタイルを覗いてみましょう。

<a href="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot20.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/11/screenshot20.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-14852" /></a>

「アウトラインメニュー」という部分をクリックしてみると、「正規表現」という項目の下に、よくわからない記号が並んでいますね。大抵の人はここで諦めるかと思いますが、もうちょっと頑張ってみましょう。

私がやりたいことは、「文の冒頭に○があったら、その行をアウトラインの項目と認定する」ということです。プレーンで文章を書いているなら、＿＿使いたい記号は別にあるかもしれませんが＿＿これぐらいのルールで事足りるでしょう。それを正規表現で書けばいいわけです。するとこうなります。

^○.*

「○」を別の記号に置き換えれば、もちろんルールも変えられます。これをさっきの「アウトラインメニュー」で設定すればそれで終了です。ちなみに私は「^○.*」と「^●.*」の二つを設定したスタイルを使っております。

もし、マークダウンの見出し指定である「### 見出し３ ###」みたいなものをルールにしたけば、もう少しややこしい記述が必要ですが、その場合は標準装備されている「MarkDown」スタイルを使いましょう。あるいは「正規表現」で検索してみてください。ちなみに、こうやって書いていますが、私は正規表現が理解できているとは言い難い状況であることを書き添えておきます。

<H3>さいごに</H3>

言うまでもありませんが、数行〜数十行の文章なら「アウトラインメニュー」なんて使わなくても問題ありません。あくまでボリューム大の文章を書く際に便利ですよ、というお話でした。

