---
title : MemoFlowyのアップデートでEvernoteへの同時送信が可能に
link : 18647
date : Wed, 27 Jul 2016 00:23:06 +0000
categories : ["0-知的生産の技術","アウトライナーで遊ぼう"]
tags : ["evernote","memoflowy","workflowy"]
draft : false
author : 倉下忠憲
---

シンプルに書こうと思う。

まず、MemoFlowyがアップデートした。ver.1.5となる。the 詳細は以下の記事をご覧頂きたい。

<a href="http://www.tjsg-kokoro.com/2016/07/26/memoflowy-ver-1-5/#3URLx-success">進化を続けるMemoFlowyが獲得した3つの新機能（MemoFlowy Ver.1.5）</a> | 単純作業に心を込めて 

注目したいのは、有料アドオンとして実装された「Evernote送信機能」だ。

WorkFlowyを操作するアプリなのに、Evernoteへ送信機能？　そう、Evernoteにも送信できるようになったのだ。しかも、同時に。

この「同時」がポイントである。言い換えれば、たったワンアクションでいい。それで一つのメモがWorkFlowyにもEvernoteにも送信される。まずはこの意義を検討してみよう。

<h3>ストックと操作のジレンマ</h3>

WorkFlowy周りがどんどん便利になるにつれ、耐え難いジレンマをいつも感じていた。文章で表現すれば、こうなる。

「ストックはEvernoteにしたい。操作はWorkFlowyでしたい」

情報の保管場所として、Evernote以外の選択はありえない。情報は一元管理するのが肝である。Webに漂うさまざまな情報と、思い付きの一行メモを何の葛藤もなく一カ所で保存してくれるツールは、やはりEvernoteなのだ。

しかし、Evernoteは断片を組み立てる機能は弱い。そこはWorkFlowyでやりたい。
※<a href="https://rashita.net/blog/?p=18568">R-style » Evernoteのノートブック内を整理するときの荒技</a>でも少し触れた。

だから私は、Evernoteに蓄積したアイデアノートを（そのノートタイトルだけ）WorkFlowyに移したこともある。これはこれで操作性が上がったのだが、「どちらがメインで、どちらがサブなのか？」という疑問が残る。その疑問は、全体の運用を危うくしてしまう。

<a href="https://rashita.net/blog/?attachment_id=18648" rel="attachment wp-att-18648"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot50-500x428.png" alt="screenshot" width="500" height="428" class="alignnone size-medium wp-image-18648" /></a>
※WorkFlowyに移植されたアイデアノート群

結局、宙ぶらりんの状態が続いていた。

<h3>動作チェック</h3>

MemoFlowyのアップデートの情報を聞いて、深いことは何も考えず、とりあえずアドオンを購入し、設定を覗いてみた。

いくつか実際にテストしてみると、非常に快適なことがわかった。面倒なことはないので日常的に運用していくことは可能だろう。でも、どうやって？

Evernoteへの送信は、ノートブックが選択でき、ノートのタイトルも選べるようだった。とりあえずデフォルトのまま使うと、日付をタイトルにしたノートが作成され、そこにどんどんメモが追記されていく形となる。PostEver的な運用と言えばわかりやすいだろうか。

設定を変更し、トピック名の指定を空欄にしておけば、一行目がタイトルとなるノートを作成してくれる。これは一般的なEvernoteメモ送信アプリと動作は近い。

私が注目したのは、PostEver的な運用法の方である。何かしら引っかかるものがあった。

<h3>仮説と実験</h3>

おそらく、ノートへの追記は、ノートブックとノートのタイトルで検索して、追記するノートを特定しているのであろう。だとすれば、別にMemoFlowyが作成するノートでなくてもいけるはずだ。タイトルの書式さえ揃えておけば、あらかじめ私が作っておいたノートであっても追記できるだろう。

テストしてみると予想通りであることがわかった。よし、一歩前進。私の眼差しは、「デイリータスクリスト」に向かっていた。

「デイリータスクリスト」は私のタスク管理の基本ツールであり、一日分のタスクをまとめて書き込んでおくためのEvernoteのノートだ。そのノートはたとえば、7月28日（木）というようなタイトルで、以下のような形になっている。

<a href="https://rashita.net/blog/?attachment_id=18649" rel="attachment wp-att-18649"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot51-500x546.png" alt="screenshot" width="500" height="546" class="alignnone size-medium wp-image-18649" /></a>
※左がスケジュール、中央がタスク、右が作業ログ。欄外はすべてフリーライティング領域

このようなノートが一年分、つまり365枚（閏年は366枚）、あらかじめEvernoteに作成してある。ここにメモを追記していくようにすれば、どうなるだろうか。

デイリータスクリストは、その日はタスクリストとして機能するが、一日を超えればそれはログとなる。実際私も、そのノートにいろいろな行動ログや作業ログを書き残している。だったら、そこにメモも追加すればいいではないか。

<h3>カスタマイズと運用</h3>

それまでのデイリータスクリストは、「7月27日(水)」のような書式でタイトルが付いていた。しかし、MemoFlowyは「07月27日(水)」のような書式である。微妙に違いがある。それに、ノートタイトルで検索しているなら、日付だけではなく年も付けておいた方が紛れが少なくなるだろう。

そこで一年分すべてのノートのタイトルを「2016年07月27日(水)」というように変更した。安心して欲しい。AppleScriptでやったので2分くらいで済んだ。

<hr />
※2016年7月27日 9:46追記

<blockquote class="twitter-tweet" data-conversation="none" data-lang="ja"><p lang="ja" dir="ltr"><a href="https://twitter.com/rashita2">@rashita2</a> Evernoteのノートのタイトル書式を「7月27日(水)」にするのでしたら、MemoFlowyの設定でトピック名を「&#39;M&#39;月&#39;d&#39;日(&#39;E&#39;)」とすれば、いけましたよ。</p>&mdash; まるみ (@marumi_app) <a href="https://twitter.com/marumi_app/status/758099976861851648">2016年7月27日</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

別にノートのタイトル変えなくてもよかったみたいです。

<hr />

ともかくこれで準備万端である。実際に使ってみると、こうなる。

<a href="https://rashita.net/blog/?attachment_id=18650" rel="attachment wp-att-18650"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot52-500x409.png" alt="screenshot" width="500" height="409" class="alignnone size-medium wp-image-18650" /></a>
※Evernote。二行目のメモは直接書いたもの。

<a href="https://rashita.net/blog/?attachment_id=18651" rel="attachment wp-att-18651"><img src="https://rashita.net/blog/wp-content/uploads/2016/07/screenshot53-500x307.png" alt="screenshot" width="500" height="307" class="alignnone size-medium wp-image-18651" /></a>
※WorkFlowy。前日のメモも見える。

これで、メモの操作場所はWorkFlowyとなり、Evernoteはその痕跡を刻む場所となった。WorkFlowyでどれだけメモを操作しても、「何年何月何日に何をどんな順番で思いついたのか」というログはEvernoteに残る。安心のバックアップ体制である。

さて、これでいいのだろうか。

<h3>さいごに</h3>

正直、この体制を作ってまだ一日目である。本当にこのスタイルが（自分にとって）効果的なのかは、判然としていない。今回の記事は、MemoFlowyの新しいバージョンアップはこう使えるよ、というアイデアをシンプルに書いただけである。

とりあえず、一つ言えることは、今回のMemoFlowyの新機能は「デジタルメモとポケット一つ原則」に一石を投じたということだ。それについての考察は、実際の運用を重ねてから書くとしよう。

あとは、同時送信先にTwitterが選択できるようになれば、ツイート中毒者の私にとっては最上である。