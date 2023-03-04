---
title : Evernoteに「手帳」を作る 2018 ver.
link : 23629
date : Mon, 01 Jan 2018 01:25:17 +0000
categories : ["evernoteの使い方"]
tags : ["evernote"]
draft : false
author : 倉下忠憲
---

あけまして、おめでとうございます。

今年の目標は「<strong>とに書く</strong>」です。

よろしくお願いします。

<h2>「手帳」の入れ替え</h2>

さて、年が変わったら、最初にやることと言えば、手帳の切り替えですね。私の場合はEvernoteの切り替えとなります。

といっても、別アカウントを作ってそこに移行するわけではなく、「一年分のノート」を新規作成するのがその作業です。

素材となるのは、Evernote社さんから提供されているありがたいテンプレート。

<a href="https://blog.evernote.com/jp/2017/12/20/58178" title="2018 年に向けて: Evernote のカレンダーテンプレート - Evernote日本語版ブログ">2018 年に向けて: Evernote のカレンダーテンプレート - Evernote日本語版ブログ</a>

これをベースに、自分用のノートをカスタマイズしていきます。

<h3>月間カレンダー</h3>

テンプレートの月間カレンダーは、美しい仕上がりになっていますが、

<a href="https://rashita.net/blog/?attachment_id=23630" rel="attachment wp-att-23630"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot.png" alt="" width="592" height="657" class="alignnone size-full wp-image-23630" /></a>

一枚のノートに12ヶ月分のノートが入っているのが多少使いづらいです。そこで、12枚の新規ノートにコピペしてきます。

<a href="https://rashita.net/blog/?attachment_id=23631" rel="attachment wp-att-23631"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-1.png" alt="" width="793" height="263" class="alignnone size-full wp-image-23631" /></a>

最近私はカードビューを愛用しているので、サムネイルに（微妙に）月が表示されるのもよいですね。

<h3>年間カレンダー</h3>

年間カレンダーは、特にいじる要素もないので、そのまま使用。ほぼ日手帳で言うところの「年間インデックス」的なページですね。ここに「その日読み終えた書籍」や「その日観た映画」なんかを記入してく予定です。年間メディアログ、ですね。

<a href="https://rashita.net/blog/?attachment_id=23632" rel="attachment wp-att-23632"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-2.png" alt="" width="701" height="603" class="alignnone size-full wp-image-23632" /></a>

<h3>週間プランナー</h3>

さて、癖のあるのが週間プランナーです。紙の手帳でもバーティカルだとかレフトだとかいろいろ種類があります。

テンプレートそのままだと、私には使いにくいので、表機能をうまく使って、自分向けにカスタマイズ。

<a href="https://rashita.net/blog/?attachment_id=23633" rel="attachment wp-att-23633"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-3.png" alt="" width="793" height="725" class="alignnone size-full wp-image-23633" /></a>

月間カレンダーと同様に、「一週間一ページ」にしても良いのですが（去年はそうしていました）、連続性を重視して今回は「四半期ごとに一ページ」の形にしてみます。つまり、合計4枚のノートで、一ノートにつき13週分の週間プランナーが入っている形です。作り方は、

・自分好みの表組みを作る
・それを13個になるまでコピペ
・完成したらそのノートを合計4枚になるまで複製

となります。少々手間ですが、まあ、気にしないでおきましょう。週番号を振っておくといかにも「時間は過ぎてるぜ！」という感覚が味わえるのでオススメです。

<a href="https://rashita.net/blog/?attachment_id=23634" rel="attachment wp-att-23634"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-4.png" alt="" width="769" height="200" class="alignnone size-full wp-image-23634" /></a>

<h3>デイリーリスト</h3>

次に、一日用のページを作りましょう。

一応、テンプレートには「デイリープランナー」も準備されているのですが、私好みではないので却下。表組み機能を使って、自分の使いやすいテンプレートを作成します。

<a href="https://rashita.net/blog/?attachment_id=23635" rel="attachment wp-att-23635"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-5.png" alt="" width="801" height="818" class="alignnone size-full wp-image-23635" /></a>

コーネル式を彷彿とさせるようなデザインとなりました。上段左が時間付きの行動ログ（出費リスト）、上段右がタスクリスト、下段が雑記用スペースです。

あとはこれを365枚複製すればOKなのですが、さすがに手間です。

というわけで、その作業はAppleScriptで行いました。ついでに、単にコピーするだけでなく、前後日へのノートリンクも付け加える形に。

<a href="https://rashita.net/blog/?attachment_id=23636" rel="attachment wp-att-23636"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-6.png" alt="" width="852" height="794" class="alignnone size-full wp-image-23636" /></a>

AppleScritpでEvernoteを操作するやり方は、「<a href="https://rashita.net/blog/?tag=%e2%89%aaapplescrpt%e3%81%a7evernote%e3%82%92%e6%93%8d%e4%bd%9c%e3%81%99%e3%82%8b%e2%89%ab" title="≪AppleScrptでEvernoteを操作する≫ – R-style">≪AppleScrptでEvernoteを操作する≫</a>」の連載を追っていただければよいかと思いますが、コードはこんな感じでした。

[code]
set oneWeek to {}
set oneWeekday to {}
set newdaynote to {}
set youbiTable to &quot;&quot;
set daynotetemp to &quot;&quot;

set daynotetemp to my settemp()

set sarchMonday to my (current date)

--来週の月曜日を探す
repeat 365 times
	if (weekday of sarchMonday as number) is 2 then
		exit repeat
	else
		set sarchMonday to sarchMonday + (1 * days)
	end if
end repeat

--月曜日の日付から、一週間のリスト作成する
repeat 365 times
	set end of oneWeek to sarchMonday
	set sarchMonday to sarchMonday + (1 * days)
end repeat

--一週間分のデイリーノートを作成
repeat with i in oneWeek
	set daydate to getMonthDay(i) --日付を取得
	set dayYoubi to getDayDate(i) --曜日を取得	
	set end of oneWeekday to daydate &amp; &quot;(&quot; &amp; dayYoubi &amp; &quot;)&quot;
	tell application &quot;Evernote&quot;
		set end of newdaynote to create note title (&quot;&#x1f4c5;&quot; &amp; daydate &amp; &quot;(&quot; &amp; dayYoubi &amp; &quot;)&quot;) with text &quot; &quot;
	end tell
end repeat

tell application &quot;Evernote&quot;
	synchronize
end tell


tell application &quot;Evernote&quot;
	set a to note link of (item -1 of newdaynote)
	
	repeat
		delay 3
		if a is not missing value then
			exit repeat
		end if
		set a to note link of (item -1 of newdaynote)
	end repeat
	
end tell

tell application &quot;Evernote&quot;
	repeat with cn from 1 to 365
		set dnote to (item (cn) of newdaynote)
		if cn is not 1 then
			set enote to &quot;&lt;a href=\&quot;&quot; &amp; note link of (item (cn - 1) of newdaynote) &amp; &quot;\&quot;&gt;&quot; &amp; title of (item (cn - 1) of newdaynote) &amp; &quot;&lt;/a&gt;&quot;
		else
			set enote to &quot;&quot;
		end if
		if cn is not 365 then
			set fnote to &quot;&lt;a href=\&quot;&quot; &amp; note link of (item (cn + 1) of newdaynote) &amp; &quot;\&quot;&gt;&quot; &amp; title of (item (cn + 1) of newdaynote) &amp; &quot;&lt;/a&gt;&quot;
		else
			set fnote to &quot;&quot;
		end if
		tell dnote to append html enote &amp; &quot;_&quot; &amp; fnote &amp; &quot;&lt;br /&gt;&quot; &amp; daynotetemp
		set aTag to tag &quot;diary&quot;
		assign aTag to dnote
	end repeat
	
end tell

--データを渡したら、曜日のタグを返すサブルーチン
on getDayDate(theDate)
	set d to (weekday of theDate as number)
	-- set dayList to {&quot;&lt;font color=\&quot;#E82E0F\&quot;&gt;日&lt;/font&gt;&quot;, &quot;月&quot;, &quot;火&quot;, &quot;水&quot;, &quot;木&quot;, &quot;金&quot;, &quot;&lt;font color=\&quot;#46D7E5\&quot;&gt;土&lt;/font&gt;&quot;}
	set dayList to {&quot;日&quot;, &quot;月&quot;, &quot;火&quot;, &quot;水&quot;, &quot;木&quot;, &quot;金&quot;, &quot;土&quot;}
	repeat with i from 1 to 7
		if i is d then
			return (item i of dayList)
			exit repeat
		end if
	end repeat
	
end getDayDate

--データを渡したら、○月○日で返すサブルーチン
on getMonthDay(theDate)
	set y to (year of theDate)
	set m to my monthNumStr(month of theDate)
	set d to day of theDate
	return (m &amp; &quot;月&quot; &amp; d &amp; &quot;日&quot;) as text
end getMonthDay

--month of dete から数字の月を返す。
on monthNumStr(theMonth)
	set monList to {January, February, March, April, May, June, July, August, September, October, November, December}
	repeat with i from 1 to 12
		if item i of monList is theMonth then exit repeat
	end repeat
	return i
end monthNumStr

on settemp()
	display dialog &quot;ok&quot;
	return &quot;&lt;table style=\&quot;border-collapse: collapse; min-width: 100%;\&quot;&gt;&lt;colgroup&gt;&lt;col style=\&quot;width: 256px;\&quot;/&gt;&lt;col style=\&quot;width: 472px;\&quot;/&gt;&lt;/colgroup&gt;&lt;tbody&gt;&lt;tr&gt;&lt;td style=\&quot;border: 1px solid rgb(185, 106, 69); background-color: rgb(231, 132, 86); width: 256px; padding: 8px;\&quot;&gt;&lt;div&gt;&lt;a href=\&quot;evernote:///view/307590/s4/60049af9-6046-4055-a1b7-430b23ddc2d9/60049af9-6046-4055-a1b7-430b23ddc2d9/\&quot;&gt;&lt;font color=\&quot;#000000\&quot;&gt;2018年総合カレンダー&lt;/font&gt;&lt;/a&gt;&lt;/div&gt;&lt;/td&gt;&lt;td style=\&quot;border: 1px solid rgb(185, 106, 69); background-color: rgb(231, 132, 86); width: 472px; padding: 8px;\&quot;&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;/td&gt;&lt;/tr&gt;&lt;tr&gt;&lt;td style=\&quot;border: 1px solid rgb(204, 201, 188); background-color: rgb(255, 251, 235); width: 256px; padding: 8px;\&quot;&gt;&lt;div&gt;起床&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;/td&gt;&lt;td style=\&quot;border: 1px solid rgb(204, 201, 188); background-color: rgb(255, 251, 235); width: 472px; padding: 8px;\&quot;&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;/td&gt;&lt;/tr&gt;&lt;tr&gt;&lt;td style=\&quot;border: 1px solid rgb(204, 201, 188); background-color: rgb(255, 251, 235); width: 728px; padding: 8px;\&quot; colspan=\&quot;2\&quot;&gt;&lt;div&gt;今日のノート&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;div&gt;&lt;br/&gt;&lt;/div&gt;&lt;/td&gt;&lt;/tr&gt;&lt;/tbody&gt;&lt;/table&gt;&quot;
	
end settemp
[/code]

もっとスマートに書けるかと思いますが、日曜大工仕事なのでその辺はスルーでお願いします。

<h3>総合カレンダー</h3>

これで、年間インデックス(1)、月間カレンダー(12)、週間プランナー(4)、デイリーノート(365）の合計382枚のノートができました。これを統合するカレンダーも作っておきます。

<a href="https://rashita.net/blog/?attachment_id=23637" rel="attachment wp-att-23637"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-7.png" alt="" width="861" height="851" class="alignnone size-full wp-image-23637" /></a>

ここにすべての「一年ページ」へのノートリンクが集まっています。で、このノートに「一年の目標」などを書き付けておくと、目に触れる回数がアップするので好感触ですね。

ちなみに、下の方には自問とマインドセットも置いてあります。

<a href="https://rashita.net/blog/?attachment_id=23638" rel="attachment wp-att-23638"><img src="https://rashita.net/blog/wp-content/uploads/2018/01/screenshot-8.png" alt="" width="817" height="383" class="alignnone size-full wp-image-23638" /></a>

<h2>おわりに</h2>

これで、「今年のノート」が一式揃いました。言い換えれば、Evernote上に「手帳」を作れたことになります。ここでは紹介しきれなかった細かい工夫もいろいろあるのですが、大まかには紹介したやり方で作れます。

最後に、（Macであれば）「総合カレンダー」をショートカットスペースに置いておけば、各ノートがどこにあっても（つまり、ノートブックがバラバラに散らばっていても）、すぐさまそれらのノートにアクセス可能となります。

作ったはいいけど、見失ってしまってなかなか見つからない、ということはよく起こりますので、まとめのページを作っておくのは妙手でしょう。

では、本年もよろしくお願いいたします。

<strong>▼こんな一冊も：</strong>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/41oyLdAhfmL._SL160_.jpg" alt="Evernote豆技50選 (Espresso Books)" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Evernote豆技50選 (Espresso Books)</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.01.01</div></div><div class="amazlet-detail">倉下忠憲 (2015-03-29)<br />売り上げランキング: 34<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B00VEEJ9XU/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>


<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/514KoiCNJ1L._SL160_.jpg" alt="ズボラな僕がEvernoteで情報の片付け達人になった理由" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">ズボラな僕がEvernoteで情報の片付け達人になった理由</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.01.01</div></div><div class="amazlet-detail">倉下 忠憲 <br />シーアンドアール研究所 (2016-02-26)<br />売り上げランキング: 109,912<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/4863541953/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>

<div class="amazlet-box" style="margin-bottom:0px;"><div class="amazlet-image" style="float:left;margin:0px 12px 1px 0px;"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01MXXFY28/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank"><img src="https://images-fe.ssl-images-amazon.com/images/I/410t4sR1ziL._SL160_.jpg" alt="「目標」の研究" style="border: none;" /></a></div><div class="amazlet-info" style="line-height:120%; margin-bottom: 10px"><div class="amazlet-name" style="margin-bottom:10px;line-height:120%"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01MXXFY28/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">「目標」の研究</a><div class="amazlet-powered-date" style="font-size:80%;margin-top:5px;line-height:120%">posted with <a href="http://www.amazlet.com/" title="amazlet" target="_blank">amazlet</a> at 18.01.01</div></div><div class="amazlet-detail">R-style (2016-12-11)<br />売り上げランキング: 3,298<br /></div><div class="amazlet-sub-info" style="float: left;"><div class="amazlet-link" style="margin-top: 5px"><a href="http://www.amazon.co.jp/exec/obidos/ASIN/B01MXXFY28/rashita1000-22/ref=nosim/" name="amazletlink" target="_blank">Amazon.co.jpで詳細を見る</a></div></div></div><div class="amazlet-footer" style="clear: left"></div></div>





