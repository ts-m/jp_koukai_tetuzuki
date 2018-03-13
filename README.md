# 日本の様式(公開)

公的手続きで必要になるいくつかの書類を、SVGとして置いています。
SVGですので任意のテキストエディタやプログラム言語で内容の修正が可能です。
Google ChromeやSafari 等ブラウザで画像として表示するか、
Inkscape、Adobe Illustrator 等で開くことができます。

SVG の構文は 互換性維持とLinuxサーバ上での容易な変換を可能にするため、
transform など、いくつかの高度な機能は意図的に使用していません。
このためところどころ冗長な記述が存在します。

[一覧](index.md)


### フォント

フォントは次の設定でちょうど合うように調整されています。
インストールされていない場合は別途入手が必要です。
無くても代替フォントで概ね表示されますが、表示が崩れる箇所があります。

- serif : IPA 明朝
- sans-serif: IPA ゴシック
- monospace: IPA ゴシック

CentOS の場合 ` yum install ipa*fonts ` で、
Ubuntu の場合 ` apt-get install otf-ipafont-gothic ` でインストールできるでしょう。

またブラウザで表示する場合は、最小フォントサイズ設定により、
小さすぎる文字が拡大されてしまう時があります。
指定を切るか、可能な限り小さな表示を有効にしてください。

### 変換

変換では [librsvg2](https://github.com/GNOME/librsvg) に含まれる、rsvg-convert の使用を想定しています。
phantomjs やchromeヘッドレスブラウザでも変換はできますが、
用紙の適切な設定が未調査です。

rsvg では次のようにしてPDFを生成できます。

```
# 1ページのみのPDFを作る場合
rsvg-convert --dpi-x=96 --dpi-y=96 -f pdf -o output.pdf  input1.svg

# 複数ページのPDFを作る場合
rsvg-convert --dpi-x=96 --dpi-y=96 -f pdf -o output.pdf  input1.svg input2.svg ...
```


### その他 注意など

書類中に記入されている人物 組織名、
あるいは電話番号などID類についてはあくまでサンプルです。
実在する特定の人物等とは関係ありません。

また書類を印字して提出するなどした場合に問題が発生したとしても責任は負えません。
特に自署が必要な署名や印章について複製した用紙は無効とみなされる場合があります。
各用紙に関連する注意事項をご確認の上ご利用ください。

