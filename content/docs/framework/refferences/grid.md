---
title: 'Grid'
linkTitle: 'Grid'
date: 2024-12-16T00:00:00+09:00
weight: 5
---

左から右に要素を並べるレイアウトを生成します。  
Horizontalとの違いは規定の個数以上は折り返して下に配置されることです。  
行と列のある格子状のレイアウトを表現できます。  
GridはYKLayoutを継承しているので、ほかの要素を子要素として生成できます。  
生成した順番に並ぶので処理の順序に注意してください。

```C#
YKGrid YKLayout.Grid()
```

## 引数
|引数|型|説明|
|--|--|--|
|なし|||


## サンプル

```C#
public override void OnLayout()
{
    var group = Grid();
}
```
