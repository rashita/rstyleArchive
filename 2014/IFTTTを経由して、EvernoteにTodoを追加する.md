---
title : IFTTTを経由して、EvernoteにTodoを追加する
link : 13350
date : Mon, 19 May 2014 00:35:46 +0000
categories : ["evernoteの使い方"]
tags : ["evernote","ifttt"]
draft : false
author : 倉下忠憲
---

知らない間にIFTTTのEvernoteチャンネルに新しいアクションが増えていました。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot9.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot9.png" alt="screenshot" width="419" height="233" class="alignnone size-full wp-image-13351" /></a>

IFTTTって何？チャンネルって？、という方は以下の記事をご覧ください。

<a href="https://rashita.net/blog/?p=12150" target="_blank">EvernoteとIFTTTのおさらい（１）　〜IFTTTとは何か〜</a>
<a href="https://rashita.net/blog/?p=12228" target="_blank">EvernoteとIFTTTのおさらい（２）　〜トリガーとアクション〜</a>

今回は新しく追加されたアクションをチェックしてみましょう。

<H3>チェックボックス付き</H3>

増えたのは「Append a to-do to note」というアクション。その中身は、

<blockquote>
This Action will append a to-do checkbox to an note as determined by its title and notebook.Once a note's size reaches 2MB a new note will be created.
</blockquote>

というもの。ざっくりまとめると、ノートにcheckboxを追加しちゃうよ。そのノートが2MBになったら新しいノートを作るよ、といったところでしょうか。

とりあえず使ってみましょう。

<H3>Make a recipes</H3>

以下のようなレシピを作りました。

<a href="https://ifttt.com/recipes/175604-addtask-to-evernote-from-twitter" target="_blank">addTask to Evernote from Twitter</a>

トリガーに選んだのはツイッター。しかもハッシュタグ付きです。「#addtodo」というハッシュタグをつけてツイートすると、そのツイート内容がEvernoteに送信されます。もちろんCheckboxとセットです。

つまり、以下のようなツイートをすると

<blockquote class="twitter-tweet" lang="ja"><p>連携テスト <a href="https://twitter.com/search?q=%23addtodo&amp;src=hash">#addtodo</a></p>&mdash; 倉下 忠憲 (@rashita2) <a href="https://twitter.com/rashita2/statuses/468178972933513216">2014, 5月 18</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

次のようなノートができるわけです。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot10.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot10.png" alt="screenshot" width="583" height="389" class="alignnone size-large wp-image-13352" /></a>


以降、#addtodo付きツイートをするたびに、このノートにどんどんチェックボックスが追加されていきます。

上記は一番シンプルな形でレシピを構成しましたが、「Append a to-do to note」の設定は、以下のようになっており、

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot11.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot11.png" alt="screenshot" width="500" height="659" class="alignnone size-large wp-image-13353" /></a>

この中にあるTo-doについては、次のような項目も扱えます。

<a href="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot12.png"><img src="https://rashita.net/blog/wp-content/uploads/2014/05/screenshot12.png" alt="screenshot" width="500" height="174" class="alignnone size-large wp-image-13354" /></a>

この中の「CreatedAt」を使えば、タスクを登録した日時も管理できますね。必要かどうかは、使う人の判断ですが。

<H3>another</H3>

この「Append a to-do to note」は、他にどのような使い方ができるでしょうか。

それを考えるためには、「どこでタスクが発生するか」を思い浮かべてみるとよいでしょう。そう、メールです。

たとえば、Gmailでメールにスターを付けたら、そのメールのタイトルがTaskとして追加される。なんてレシピはありそうです。スターの代わりに、特定のラベルを付ける、というのもアリでしょう。

ラベルなら、こういうレシピになります。

<a href="https://ifttt.com/recipes/175607-todo-mail-to-evernote" target="_blank">todo @mail to Evernote</a>

あるいは、他のタスク管理ツールと連携させて何かできるかもしれません。そのあたりは、ご自分でお試しくださいませ。

<H3>さいごに</H3>

ちょっとしたタスクの追加であれば、iPhoneアプリを使えば簡単に行えるわけですが、IFTTTを使うと、同じノートにタスクを追加していけるのがポイントですね。

また、メールレシピのように半ば自動的に（つまり、これをタスクリストに追加しようと思わなくても）リストに追加されるのも、案外大きなポイントです。

もちろん、こうして作成したノートを参照しなければ、まったく意味がないのは言うまでもありませんが。

<strong>▼参考リンク：</strong>
<a href="http://blog.ifttt.com/post/76537499699/introducing-the-push-co-channel-plus-new-evernote" target="_blank">Introducing the Push.co Channel! Plus, new Evernote Recipes</a>（IFFFT Blog）