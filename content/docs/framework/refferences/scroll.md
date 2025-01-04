---
title: 'Scroll'
linkTitle: 'Scroll'
date: 2024-12-16T00:00:00+09:00
weight: 4
---

Verticalと同様に要素を縦に積み上げる（ぶら下げる？）レイアウトを生成します。  
Scrollはスクロール可能な要素で、高さが上限に達するとスクロールバーが表示され、マウスホイールでスクロールが可能になります。  
ScrollはYKLayoutを継承しているので、ほかの要素を子要素として生成できます。  
生成した順番に並ぶので処理の順序に注意してください。

```C#
YKScroll YKLayout.Scroll()
```

## 引数
|引数|型|説明|
|--|--|--|
|なし|||


## サンプル

```C#
public override void OnLayout()
{
    var group = Scroll();
}
```
