---
title: 'Vertical'
linkTitle: 'Vertical'
date: 2024-12-16T00:00:00+09:00
weight: 2
---

要素を縦に積み上げる（ぶら下げる？）レイアウトを生成します。  
VerticalはYKLayoutを継承しているので、ほかの要素を子要素として生成できます。  
生成した順番に並ぶので処理の順序に注意してください。

```C#
YKVertical YKLayout.Vertical()
```

## 引数
|引数|型|説明|
|--|--|--|
|なし|||


## サンプル

```C#
public override void OnLayout()
{
    var group = Vertical();
}
```
