---
title: 'LayoutH'
linkTitle: 'Horizontal'
date: 2024-12-16T00:00:00+09:00
weight: 3
---

左から右に要素を並べるレイアウトを生成します。
LayoutVはLayoutBaseを継承しているので、ほかの要素を子要素として生成できます。  
生成した順番に並ぶので処理の順序に注意してください。

```C#
LayoutH Window.Horizontal()
LayoutH LayoutBase.Horizontal(float? size = null)
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
    var horizontal = window.Horizontal();

    return this;
}
```
