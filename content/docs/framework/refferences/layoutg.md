---
title: 'LayoutG'
linkTitle: 'Grid'
date: 2024-12-16T00:00:00+09:00
weight: 5
---


```C#
LayoutG LayoutBase.Grid(float? size = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|size|float|固定する場合のサイズ（幅と高さのどちらが対象かは親要素次第）|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var grid = layout.Grid();

    return this;
}
```
