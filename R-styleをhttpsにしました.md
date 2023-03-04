---
title : R-styleをhttpsにしました
link : 22517
date : Mon, 17 Jul 2017 02:22:22 +0000
categories : ["blogarts"]
tags : []
draft : false
author : 倉下忠憲
---

以下のニュースを見て、おおっ、と思ったので早速設定してみました。

<a href="http://internet.watch.impress.co.jp/docs/news/1070001.html">ロリポップ！利用者向けにLet's Encryptの無料SSL証明書発行サービスを提供、GMOペパボ -INTERNET Watch</a>

設定自体はものすごく簡単です。

<a href="https://lolipop.jp/manual/user/ssl-free-order/">独自SSLのお申込み・設定方法（無料） / セキュリティ / マニュアル - レンタルサーバーならロリポップ！</a>

ボタンをポチっで、5分ほどでhttps://でのアクセスが可能となりました。問題はここからです。このR-styleはWordPressシステムを使っているので、その対応も必要です。

WordPressのSSL化対応は、以下の記事が参考になりました。

<a href="https://nelog.jp/wordpress-ssl">WordpressをhttpからhttpsにSSL化した全手順まとめ（エックスサーバー環境）</a>

実際にやったことは、

<ul>
<li>バックアップを取っておく</li>
<li>Wordpress管理画面で「WordPressアドレス」と「サイトアドレス」を書き換える</li>
<li>サイト内のhttp://rashita.net/blogをhttps://rashita.net/blogに置換する</li>
<li>http://rashita.net/blogに来たアクセスをhttps://rashita.net/blogに飛ばす</li>
</ul>

の四つ。

バックアップについては、以下を参考にロリポップからphpMyAdminにアクセスしてデータベースと、サイトに上げてあるファイル全てを保存しておきました。途中大きな変更を加える箇所があるので、バックアップは必須です。

<a href="https://wpdocs.osdn.jp/WordPress_%E3%81%AE%E3%83%90%E3%83%83%E3%82%AF%E3%82%A2%E3%83%83%E3%83%97">WordPress のバックアップ - WordPress Codex 日本語版</a>

で、Wordpress管理画面の書き換えは、sを二つ足すだけなので、簡単です。

<a href="https://rashita.net/blog/?attachment_id=22519" rel="attachment wp-att-22519"><img src="https://rashita.net/blog/wp-content/uploads/2017/07/screenshot-4-500x251.png" alt="" width="500" height="251" class="alignnone size-medium wp-image-22519" /></a>
問題は次。記事の中にあるhttp://rashita.net/blog/*へのリンクをhttps://rashita.net/blog/*に書き換える必要があります。一つひとつの記事を編集していくのは、4800記事ほどある当ブログでは現実的ではないので、「Search Regex」というWordPressのプラグインを使いました。記事を対象とした一括置換を実現してくれるプラグインです。

<a href="https://ja.wordpress.org/plugins/search-regex/">Search Regex — WordPress プラグイン</a>

が、ここで問題が生じました。http://rashita.net/blog/→https://rashita.net/blog/を置換しようとすると、エラーが出るのです。エラーメッセージをざっくり読むと、「数が多すぎるぞ」というもの。「そんなこと言われても……」と途方に暮れかけていたら、次の記事を見つけました。

<a href="http://nekokick3.com/wordpress/2016/06/30/https-searchregex/">【https化】リダイレクトプラグインSearch Regexエラーの原因と改善方法 | 人つなげ屋さん上條晴行.com</a>

一括で置換しようとするのが数が多すぎるのならば、小分けにすればいいんじゃない、という提案です。なるほど。さっそく、

・http://rashita.net/blog/?attachment_id→https://rashita.net/blog/?attachment_id

で置換すると、うまくいきました。同様に、

・http://rashita.net/blog/?p=1→https://rashita.net/blog/?p=1
・http://rashita.net/blog/?p=2→https://rashita.net/blog/?p=2

など、いくつかのフィルタリングで変換を行い、ある程度減ってきたところで、

・http://rashita.net/blog/→https://rashita.net/blog/

を実行。今度はエラーも表示されず、うまくいきました。めでたしめでたし。

あとは、ウィジェットや.phpファイルに直接書き込んであるhttp://rashita.net/blog/をhttps://rashita.net/blog/に書き換えるなどして、移行は完了です。

最後に、http://rashita.net/blog/にアクセスしてきた人に、https://rashita.net/blog/に回ってもらう処理を、.htaccessに記述してアップロードして終了です。この辺の手順は、最初に紹介した記事の通りでうまくいきました。

というわけで、ロリポップでWordPressを動かしている人は、結構簡単にSSL化できますので、チャレンジしてみてはいかがでしょうか。
