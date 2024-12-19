---
title: 'UI要素（Element）作成'
linkTitle: 'UI要素の作成'
date: 2024-12-16T00:00:00+09:00
weight: 3
---

とてもシンプルな例とともにUI要素の配置について説明します。
UIの構造はツリー状のような構造で表現されます。

次の例では縦にテキストの「表示するテキスト１」「表示するテキスト２」と、ボタンの「ボタンのテキスト」が並ぶ構成です。

```C#
var window = this.Window(640, 480, "カスタムウィンドウ");
var layout = window.Vertical();
layout.Text("表示するテキスト１");
layout.Text("表示するテキスト２");
layout.Button("ボタンのテキスト", () => { Debug.Log("Pressed!"); });
```

構造を図で示すと次のようになります。

```mermaid
graph LR;
    Window-->Vertical;
    Vertical-->Text1;
    Vertical-->Text2;
    Vertical-->Button;
```

順序は宣言した順になるので、ボタンなどのインタラクティブな要素で、ほかの要素を参照する処理が必要な場合は注意が必要です。  
次の例のようにあらかじめ変数`text`を宣言して対応します。

```C#
var window = this.Window(640, 480, "カスタムウィンドウ");
var layout = window.Vertical();
layout.Text("表示するテキスト１");
UIHost<UIText> = text;
layout.Button("ボタンのテキスト", () => { /* 変数[text]をゴニョゴニョする */ });
text = layout.Text("表示するテキスト２");
```

例に挙げた`Vertical`や`Text`意外にもたくさんのUI要素が用意されています。

これらは[リファレンス]({{% relref "refferences/_index.md" %}})で詳細を確認できます。
