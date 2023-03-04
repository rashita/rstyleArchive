---
title : DQNが不得意だったゲーム
link : 15865
date : Thu, 16 Apr 2015 04:34:10 +0000
categories : ["2-社会情報論"]
tags : []
draft : false
author : 倉下忠憲
---

少し前、Googleの人工知能アルゴリズム「DQN」が話題になっていた。

<a href="http://www.itmedia.co.jp/news/articles/1502/26/news109.html" target="_blank">Googleの人工知能「DQN」、アタリゲームで人間よりハイスコア叩き出す</a>（ITmedia）

<blockquote>米GoogleのDeepMindチームは2月25日（現地時間）、人工知能（AI）アルゴリズム「deep Q-network（DQN）」についての論文を発表した。DQNはゼロからゲームのルールを学習し、「Breakout」や「Pong」（ブロック崩し）などの「Atari 2600」の2次元ビデオゲームで最終的には人間よりハイスコアを獲得するまでに成長した。</blockquote>

素晴らしい成果である。

もちろん、アルゴリズムがハイスコアを出しただけならたいしたことではない。専用のアルゴリズムを組んでおけば良いだけだ。そして、それではそのゲームをプレイしているのは人間に留まってしまう。あくまで機械に代替させているだけ。

しかし、DQNは、自らの体験による学習で、ゲームのプレイ方法を学んでいった。ブロック崩しは比較的単純なシチュエーションと言えるが、今後より複雑な状況に対応できるようになれば、現実世界で動くロボットのアルゴリズムにも少なからずの影響を与えるだろう。

そのように、今後の成長が期待できるAIではあるのだが、いくつかの紹介記事を見ていて気になったことがあった。

<a href="http://wired.jp/2015/02/28/google-deepmind-atari/" target="_blank">ゲーム攻略で人間を超えた人工知能、その名は「DQN」</a>（WIRED）

<a href="http://www.nikkei.com/article/DGXLZO83685140W5A220C1EA2000/" target="_blank">グーグル、自ら学ぶ人工知能開発　ゲーム繰り返し遊んで攻略</a>（日本経済新聞）

49種類のゲームのうち、29種類のゲームで人間並みかそれ以上の得点をたたき出したという。素晴らしい成果だ。じゃあ、それ以下のゲームってどのようなものだったのだろうか。つまり、時間をかけてもDQNがうまくならなかったゲームって、どんなタイプのゲームなのだろうか。ゲーム好きとしては気になってくる。

<a href="http://googleresearch.blogspot.jp/2015/02/from-pixels-to-actions-human-level.html" target="_blank">From Pixels to Actions: Human-level control through Deep Reinforcement Learning</a>（Google Research Blog）

上の記事では、ゲームのタイトルと成績がグラフでまとめられている。できれば、直接記事をご覧頂きたいが、一部分だけ引用させていただく。人間よりも成績が下回った部分だ。

<a href="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot6.png"><img src="https://rashita.net/blog/wp-content/uploads/2015/04/screenshot6.png" alt="screenshot" width="500" height="" class="alignnone size-full wp-image-15868" /></a>

残念ながらタイトルが英語なので、ゲームについてはちんぷんかんぷんである。しかし、いくつか推測が働くものもある。たとえば、「Double Dunk」はバスケットのゲームだろう。そして、タイトルさえわかればググれる。キーワードにatariをつければ、だいたいのゲーム動画が見つかる。

<iframe width="420" height="315" src="https://www.youtube.com/embed/KLgrEhProOc" frameborder="0" allowfullscreen></iframe>

よくわからないが、2on2のバスケットゲームのようだ。

あるいは、「Ms. Pac-Man」というものもある。これはもちろん、パックマンのことだろう。

<iframe width="420" height="315" src="https://www.youtube.com/embed/cVH1mCc5EvU" frameborder="0" allowfullscreen></iframe>

他にも「Seaquest」という潜水艦（のようなもの）を操縦して、海洋生物と戦うゲームもあった。

ブロック崩しやピンボールと、これらのゲームの違いは何であろうか。単純に考えれば、複雑性である。

ブロック崩しで、プレイヤーがすべきこと（できること）は、バーを左右に移動させるだけだ。そして、注意を絞るのはボールの動きだけでいい。ボールの位置とベクトルさえ把握しておけば、ボールに近づくように（離れすぎないように）できるし、それでゲームは続けられる。

DQNが優秀な成績を収めた他のゲームでも事情は似通っている。

縦スクロールのシューティング「River Raid」では、自機は左右にしか動かない、ボクシングゲームの「Boxing」は四角のリングを自由に動き回れるが相手は一人で、しかも攻撃は平面からのみ。かがんでからのアッパーも、打ち下ろしのチョッピングライトも飛んでこない。3Dのカーレース「Enduro」は、見た目は立体だがゲームとしては細い縦スクロールシューティングと大差がない。競争相手はたくさんいるが、意識するのは少し前を走る車だけでよい。

それに比べるとDQNが不得意としたゲームは、状況が複雑である。

「Double Dunk」は自由に動き回れる上、相手も二人、自分たちも二人である。行動の選択肢もドリブルがあり、パスがあり、シュートがある。

「Ms. Pac-Man」は、動きこそ通路で制約されているが、経路は無数に存在する。挙げ句の果てに強力な敵がわんさか存在し、それらがリアルタイムで動いている。そして、その動きはランダムとパターンが微妙に組み合わさっている。

行動の選択肢がたくさんあり、しかも、その結果に点を付けにくい。

ある状況でAという行動を取りました。結果の成績が1000点でした。同じ状況で今度はBという行動を取り、結果が2000点でした。次からはBという行動を取ります。という、状況であれば「進化」は早いだろう。

しかしながら、パックマンでは同じ状況の再現性はほとんどない。主人公の敵キャラの位置関係ならばいくらでも再現性はあるが、残りの敵の位置、残っているアイテムの数や場所は変わってしまう。かといって、「最短でアイテムを集めきる」という戦略をとると（ご存じのように）即死してしまうし、「敵に接触する可能性がある行動をとらない」ようになると身動きできなくなる。

目の前の状況に対応しながら、全体の状況も考慮しなければならないし、また違った風にみえる状況からパターンを見つけ出し、使えるテクニックを選択しなければならない。

もちろん、そうしたことが人工知能にまったく不可能だ、という話をしたいわけではない。多体問題的な難しさを含むかもしれないが、進化の可能性はいつでもある。

が、それはそれとしてフィードバックサイクルと評価の問題は意識しておきたい。

ある行動を取り、その結果が即時的に「良い」というフィードバックを返すものならば、その進化・進歩は容易い。アルゴリズムでも達成されているのだ（もちろん、その技術が易しいと言っているわけではない）。

しかし、行動とその結果の関係が見えにくいものだったり、フィードバックが返ってくるのが相当後になるものだったり、あるいはそもそも明確な点数付けなどできないものであるとき（「私はこの小説に92点ほど感動しました」）、その進化・進歩は容易いものではなくなる。少なくとも、その取り扱いには慎重さが求められる。

その扱い方こそが我々とDQNを分ける、と言いたいところだが、それは楽観過ぎるというものだろう。少なくとも、「今のところ」という留保は必要だし、そもそもとして、私たちが本当にそうしたものの扱いに長けているかも疑問である。

しかし、そうしたアプローチでしか解決・達成できない問題や課題が存在するのならば、軽んじてはいけないだろう。

<strong>▼こんな一冊も：</strong>

<table  border="0" cellpadding="5"><tr><td colspan="2"><a href="http://www.amazon.co.jp/%E3%83%9E%E3%83%83%E3%83%81%E7%AE%B1%E3%81%AE%E8%84%B3-AI-%E2%80%95%E4%BD%BF%E3%81%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD%E3%81%AE%E3%81%8A%E8%A9%B1-%E6%A3%AE%E5%B7%9D%E5%B9%B8%E4%BA%BA-ebook/dp/B00DT4DY0M%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00DT4DY0M" target="_blank">マッチ箱の脳(AI)―使える人工知能のお話</a><img src="http://www.assoc-amazon.jp/e/ir?t=rashita1000-22&l=ur2&o=9" width="1" height="1" style="border: none;" alt="" /></td></tr><tr><td valign="top"><a href="http://www.amazon.co.jp/%E3%83%9E%E3%83%83%E3%83%81%E7%AE%B1%E3%81%AE%E8%84%B3-AI-%E2%80%95%E4%BD%BF%E3%81%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD%E3%81%AE%E3%81%8A%E8%A9%B1-%E6%A3%AE%E5%B7%9D%E5%B9%B8%E4%BA%BA-ebook/dp/B00DT4DY0M%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00DT4DY0M" target="_blank"><img src="http://ecx.images-amazon.com/images/I/41mWulcvpoL._SL160_.jpg" border="0" alt="マッチ箱の脳(AI)―使える人工知能のお話" /></a></td><td valign="top"><font size="-1">森川幸人 <br /><br />森川幸人  2014-01-05<br />売り上げランキング : 2100<br /><br /><br /><a href="http://www.amazon.co.jp/%E3%83%9E%E3%83%83%E3%83%81%E7%AE%B1%E3%81%AE%E8%84%B3-AI-%E2%80%95%E4%BD%BF%E3%81%88%E3%82%8B%E4%BA%BA%E5%B7%A5%E7%9F%A5%E8%83%BD%E3%81%AE%E3%81%8A%E8%A9%B1-%E6%A3%AE%E5%B7%9D%E5%B9%B8%E4%BA%BA-ebook/dp/B00DT4DY0M%3FSubscriptionId%3D15SMZCTB9V8NGR2TW082%26tag%3Drashita1000-22%26linkCode%3Dxm2%26camp%3D2025%26creative%3D165953%26creativeASIN%3DB00DT4DY0M" target="_blank">Amazonで詳しく見る</a></font><font size="-2"> by <a href="http://www.goodpic.com/mt/aws/index.html" >G-Tools</a></font></td></tr></table>
