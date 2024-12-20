---
title: 'Header'
linkTitle: 'Header'
date: 2024-12-16T00:00:00+09:00
weight: 101
---

装飾されたテキストを生成します。

```C#
UIHost<UIItem> LayoutBase.Header(string text, Sprite? sprite = null, string headerType = "Note", float width = 210f)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|テキスト|
|sprite|Sprite|テキストの頭に付けるアイコン|
|headerType|string|Note、Card、Topicのいずれか|
|width|float|横幅|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var header = layout.Header("ヘッダー１");

    return this;
}
```
