---
title: 'LayoutS'
linkTitle: 'Scrollable'
date: 2024-12-16T00:00:00+09:00
weight: 4
---

LayoutVと同様に要素を縦に積み上げる（ぶら下げる？）レイアウトを生成します。  
LayoutSはスクロール可能な要素で、高さが上限に達するとスクロールバーが表示され、マウスホイールでスクロールが可能になります。  
LayoutSはLayoutBaseを継承しているので、ほかの要素を子要素として生成できます。  
生成した順番に並ぶので処理の順序に注意してください。

```C#
LayoutBase Window.Scrollable()
LayoutS LayoutBase.Scroll(float? height = null)
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
    var scrollable = window.Scrollable();

    return this;
}
```
