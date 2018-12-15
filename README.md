## PanCake コマンド一覧

PanCake で使用できる命令を一覧しています。\
PanCake 0.8 以降のファームウェア対応です。\
PanCake 0.5 が存在しますが、ネット上では公開されていないため、\
これを考慮する必要はありません。\
PCN として商品販売をはじめているのは PanCake 0.9 からとなります。

Download ZIP でファイル一覧をダウンロードできます。\
GitHub・Git を使っている場合は Clone を使っても良いでしょう。

RAW で参照した場合、またファイルをダウンロードした場合\
.txt ファイルは文字コード UTF-8、改行コード CR+LF になります。\
（2016年5月14日より文字コードを変更しました）\
Windows ではメモ帳を使用する事が可能です。

* PanCake (公式) http://pancake.shizentai.jp/
* IchigoJam (公式) http://ichigojam.net/
* イチゴジャム レシピ (公開元) https://15jamrecipe.jimdo.com/

### PanCakeプチコン３号Edition について

PanCakeプチコン３号Edition は背景画像・スプライトが\
ニンテンドー3DS 版「プチコン３号」より得られた\
キャラクターと画像に変更されています。\
コマンドそのものは PanCake 1.0 と同じ動作となります。

* PanCakeプチコン３号Edition (公式) http://panpetit.shizentai.jp/

PanCakeプチコン３号Edition: (C)PCN (C)SmileBoom Co.Ltd.\
SmileBoom、プチコン３号 は 株式会社スマイルブーム の登録商標です。

### PDF 版

西澤 眞人さんが PDF 化した IchigoJam+PanCakeコマンドリファレンス を\
Facebook グループ IchigoJam-FAN 内で公開しています。\
紙面で一覧したい場合はこちらを印刷し、ご利用下さい。

https://www.facebook.com/groups/ichigojam/626631837476573/

### バイナリコマンド

PanCake では文字列でコマンドを送る以外に\
バイナリコマンドが存在します。

記載例: 色番号 10（水色）で画面を消去する（PANCAKE CLEAR 0A）\
```
128 4 0 10 または
#80 #04 #00 #0A
```

これは Pancake 付属ドキュメント readme.txt では\
16進数表記で記載されています。この本書では # を頭に付けた値です。

```
80 04 00 0A
```

しかし、IchigoJam が当初16進数変換に対応していなかったため、\
この文章では10進数のキャラクターコードも記載しています。

これを IchigoJam から PanCake へ送る場合は\
例えば次のようになります。

```
PRINT CHR$(128,4,0,10);
PRINT CHR$(#80,#04,#00,#0A);
```

; はなくても構いません。余計な部分は PanCake は無視します。



### IchigoJam BASIC 1.1 以降で使用する場合の注意

IchigoJam BASIC 1.1 beta（1.0.2 beta9～11 を含む）より\
カーソル移動・画面クリア・スクロールなどを\
コントロールコードでシリアル送出する仕様になりました。\
PanCake 1.0 までにこの仕様を反映していないため、\
コントロールコードを受け取る事で動作が停止する場合があります。

この対処として、IchigoJam BASIC 1.0.2 beta 11 より\
UART コマンドが追加されているため、\
UART 1 を予め実行してから PanCake のコマンド送出を行って下さい。

IchigoJam BASIC 1.0.2 beta 12 は 1.0.1 を継承しているため、\
上記の対象外となります。\
ただし、このバージョンを継承した正式版は公開されていません。\
（IchigoJam BASIC 1.0.2 beta 11→1.1 beta→1.1.1 が正式公開されています）

### ライセンス

この文章は CC BY-NC で公開されている PanCake のページや\
Pancake 付属ドキュメント readme.txt\
Facebook グループ「IchigoJam-FAN」「PanCake-FAN」などの情報を元に\
志賀 慶一 (ふうせん Fu-sen.) が独自に文章化しているものです。

- Facebook グループ IchigoJam-FAN<br />https://www.facebook.com/groups/ichigojam/ \
- Facebook グループ IchigonQuest,IchigoLatte,etc-FAN<br />https://www.facebook.com/groups/568222796651326/

製作・公開公開にあたり、PanCake の著作者となる\
株式会社ナチュラルスタイル (NaturalStyle Co. Ltd.) より\
製作・公開許可をいただいています。

NaturalStyle Co. Ltd. http://na-s.jp/

Maked by 志賀 慶一 (ふうせん Fu-sen.) | Keiichi SHIGA ( BALLOON a.k.a. Fu-sen. ), 2015-2018.

<a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/"><img alt="クリエイティブ・コモンズ・ライセンス" style="border-width:0" src="https://i.creativecommons.org/l/by-nc/4.0/80x15.png" /></a>

この 文章 は <a rel="license" href="http://creativecommons.org/licenses/by-nc/4.0/">クリエイティブ・コモンズ 表示 - 非営利 4.0 国際</a> (CC BY-NC 4.0) ライセンスで\
提供しています。
