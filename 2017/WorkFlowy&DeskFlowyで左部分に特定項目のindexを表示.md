---
title : WorkFlowy&DeskFlowyで左部分に特定項目のindexを表示
link : 22817
date : Fri, 01 Sep 2017 02:45:30 +0000
categories : ["アウトライナーで遊ぼう"]
tags : ["deskflowy","workflowy"]
draft : false
author : 倉下忠憲
---

以前、以下の記事を書きました。

<a href="https://rashita.net/blog/?p=22733">WorkFlowyの左部分に特定項目のindexを表示 – R-style</a>

個人的には便利に使っているものの、導入までのステップがちょっと初心者向きではないので、どうしようかな〜と思っていた矢先、DeskFlowyの登場です。

<a href="https://rashita.net/blog/?p=22793">WorkFlowy専用クライアントソフト「DeskFlowy」 – R-style</a>

DeskFlowyでは、何の拡張機能もインストールすることなく、直にJavaScriptでの拡張が可能です。だったら、初心者でもぜんぜんOKですね。というわけで、以前紹介したIndex表示を、DeskFlowyにて実装してみましょう。

<h2>Extension Script</h2>

使うのは、右側のサイドバーの「Extension Script」です。そこのペンマークをクリックし、テキストエリアを表示させたのち、以下のスクリプトをコピペしてください。

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
        indexMaker(/^#+? /,'header');

       }

        if (keyCode === 70 &amp;　event.shiftKey === true) {
             if(e.preventDefault){
			// デフォルトの動作を無効化する
			e.preventDefault();
             }else{
			// デフォルトの動作を無効化する（非標準）
			return false;
             }
            indexMaker(/^&#x1f4d9;/,'index');
        }

        if (keyCode === 72 &amp;　event.shiftKey === true) {
             if(e.preventDefault){
                 // デフォルトの動作を無効化する
                 e.preventDefault();
             }else{
                 // デフォルトの動作を無効化する（非標準）
                 return false;
             }
            indexMaker(/^&#x1f4d8;/,'project');
        }

};

function indexMaker(reg,title){
    p=pageContainer.innerHTML.replace(/\n/g, '%#10').replace(/&amp;amp;/g,&quot;&amp;&quot;).replace(/&amp;nbsp;/g,&quot;&quot;).replace(/&lt;div class=&quot;project/g,'\n&lt;div class=\&quot;project').replace(/&lt;span class=&quot;parentArrow&quot;&gt;/g, '\n&lt;span class=\&quot;parentArrow\&quot;&gt;');
    line = p.split('\n');
    var outtxt=&quot;&quot;;
    for (i = 0; i &lt; line.length; i++) {
        c = line[i];
        if(c!==''){
            switch (true) {
                case /&lt;div class=&quot;project/.test(c):
                    tempX = c.replace(/.*?projectid=&quot;.*?-.*?-.*?-.*?-(.*?)&quot;.*?&lt;div class=&quot;content&quot;.*?&gt;(.*?)&lt;\/div&gt;/g,'$2').replace(/&lt;span class=&quot;contentBold contentItalic contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentBold contentItalic&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentBold contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentItalic contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentBold&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentItalic&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;a class=&quot;contentLink&quot;.+?&gt;(.+?)&lt;\/a&gt;/g,'$1').replace(/&lt;span class=&quot;contentTag&quot;.+?&gt;.+?&lt;\/span&gt;&lt;\/span&gt;/g, '').replace(/&lt;span class=&quot;contentMatch.+?&gt;(.+?)&lt;\/span&gt;/g,'$1');
                    if  (reg.test(tempX)){
                        outtxt += c.replace(/.*?projectid=&quot;.*?-.*?-.*?-.*?-(.*?)&quot;.*?&lt;div class=&quot;content&quot;.*?&gt;(.*?)&lt;\/div&gt;/g,'&lt;a href=&quot;https://workflowy.com/#/$1&quot;&gt;$2&lt;\/a&gt;').replace(/&lt;span class=&quot;contentBold contentItalic contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentBold contentItalic&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentBold contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentItalic contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentBold&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentItalic&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;span class=&quot;contentUnderline&quot;&gt;(.+?)&lt;\/span&gt;/g, '$1').replace(/&lt;a class=&quot;contentLink&quot;.+?&gt;(.+?)&lt;\/a&gt;/g,'$1').replace(/&lt;span class=&quot;contentTag&quot;.+?&gt;.+?&lt;\/span&gt;&lt;\/span&gt;/g, '').replace(/&lt;span class=&quot;contentMatch.+?&gt;(.+?)&lt;\/span&gt;/g,'$1')+&quot;\n&quot;;
                    }
                break;
                default:
                    break;
            }
        }
    }
    outtxt=outtxt.replace(/\n/g,'&lt;br /&gt;\n');
    var e=document,a=e.getElementById(&quot;_wf_index&quot;);
    a&amp;&amp;e.body.removeChild(a);
    a=e.createElement(&quot;div&quot;);
    a.id=&quot;_wf_index&quot;;
    a.innerHTML=&quot;&lt;p style=\&quot;font-size:12px\&quot;&gt;&quot; + title + &quot;&lt;br /&gt;&quot; + outtxt+ &quot;&lt;/p&gt;&quot;;
    a.setAttribute(&quot;style&quot;,&quot;background-color:#fff;border:1px solid #ccc;opacity:1.0;position:fixed;top:50px;left:10px;z-index:10;width:200px;height:auto;font-size:11px;padding:5px&quot;);
    e.body.appendChild(a);
}

[/javascript]


<a href="https://rashita.net/blog/?attachment_id=22821" rel="attachment wp-att-22821"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-1.png" alt="" width="198" height="793" class="alignnone size-full wp-image-22821" /></a>


その後、フロッピーディスクっぽい保存ボタンを押して、再生っぽい実行ボタンを押します。これで準備OK.

<a href="https://rashita.net/blog/?attachment_id=22820" rel="attachment wp-att-22820"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot.png" alt="" width="202" height="170" class="alignnone size-full wp-image-22820" /></a>

<h2>３つの表示</h2>

スクリプトがうまく動いているならば、３つのショートカットキーが使えるようになります。

shift + f

<a href="https://rashita.net/blog/?attachment_id=22822" rel="attachment wp-att-22822"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-2-500x327.png" alt="" width="500" height="327" class="alignnone size-medium wp-image-22822" /></a>

行頭に&#x1f4d9;がある項目を拾ってindexを作成します。私は、企画案の卵（あるいは核）のような項目にこの絵文字をつけています。


shift + g

<a href="https://rashita.net/blog/?attachment_id=22823" rel="attachment wp-att-22823"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-3-500x297.png" alt="" width="500" height="297" class="alignnone size-medium wp-image-22823" /></a>

行頭に#が一つ以上ついた、いわゆるマークダウン的な見出しの項目を拾ってindexを作成します。構造的文章を書くときに便利です。

shift + h

<a href="https://rashita.net/blog/?attachment_id=22824" rel="attachment wp-att-22824"><img src="https://rashita.net/blog/wp-content/uploads/2017/09/screenshot-4-500x329.png" alt="" width="500" height="329" class="alignnone size-medium wp-image-22824" /></a>

行頭に&#x1f4d8;がある項目を拾ってindexを作成します。私は、プロジェクトの項目にこの絵文字をつけています。

絵文字などについては、コピペしたコードの中の対応する部分を置き換えれば、別の絵文字や記号にすることも可能です。その辺はお好みでどうぞ。

あと、一度表示させたindexを削除する、という機能はありませんので、うっとうしければリロードで消してください。

<h2>まとめ</h2>

上記のように、DeskFlowyのおかげで、拡張のためのJavaScriptを気楽に紹介できるようになったのですが、そもそも優れたブックマーク機能が標準装備されているので、のindexいらなくね？　みたいな疑問もないではありません。まあ、# を拾って見出しを表示されるやつは、結構便利です。WokrFlowyで文章を書いている人なんかは、一応頭に入れておくとよいかもしれません。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51HoJpXhvnL._SL160_.jpg" alt="アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">アウトライナー実践入門　～「書く・考える・生活する」創造的アウトライン・プロセッシングの技術～</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.01</div></div><div class="amazlet-detail">技術評論社 (2016-07-09)<br />売り上げランキング: 47,657<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01I0TZWUK/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:20px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/51ymv5zS94L._SL160_.jpg" alt="クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">クラウド時代の思考ツールWorkFlowy入門 (OnDeck Books（NextPublishing）)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 17.09.01</div></div><div class="amazlet-detail">インプレスR&D (2016-01-29)<br />売り上げランキング: 52,493<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01AXRCDU4/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>
