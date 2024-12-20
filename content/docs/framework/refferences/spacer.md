---
title: 'Spacer'
linkTitle: 'Spacer'
date: 2024-12-16T00:00:00+09:00
weight: 301
---

何も表示されない要素を生成します。  
要素間の余白作りに使用します。

```C#
UIHost<LayoutElement> LayoutBase.Spacer(int sizeY = 0, int sizeX = 1)
```

## 引数
|引数|型|説明|
|--|--|--|
|sizeY|int|縦方向のサイズ|
|sizeX|int|横方向のサイズ|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var space = layout.Spacer(50);

    return this;
}
```
