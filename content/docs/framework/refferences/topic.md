---
title: 'Topic'
linkTitle: 'Topic'
date: 2024-12-16T00:00:00+09:00
weight: 102
---

２つのテキストを並べて表示する要素を生成します。
ステータス能力のように名前＋ベース値のように表示される個所で使用されています。

```C#
UIHost<UIItem> LayoutBase.Topic(string text, string? value = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|左側に表示するテキスト|
|value|string|右側に表示するテキスト|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var topic = layout.Topic("テキスト１", "テキスト２");

    return this;
}
```
