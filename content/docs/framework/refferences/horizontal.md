---
title: 'Horizontal'
linkTitle: 'Horizontal'
date: 2024-12-16T00:00:00+09:00
weight: 3
---

左から右に要素を並べるレイアウトを生成します。  
HorizontalはYKLayoutを継承しているので、ほかの要素を子要素として生成できます。  
生成した順番に並ぶので処理の順序に注意してください。

```C#
YKHorizontal YKLayout.Horizontal()
```

## 引数
|引数|型|説明|
|--|--|--|
|なし|||


## サンプル

```C#
public override void OnLayout()
{
    var group = Horizontal();
}
```
