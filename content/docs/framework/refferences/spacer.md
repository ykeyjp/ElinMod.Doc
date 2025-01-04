---
title: 'Spacer'
linkTitle: 'Spacer'
date: 2024-12-16T00:00:00+09:00
weight: 301
---

何も表示されない要素を生成します。  
要素間の余白作りに使用します。

```C#
UIHost<LayoutElement> LayoutBase.Spacer(int height, int width = 1)
```

## 引数
|引数|型|説明|
|--|--|--|
|height|int|縦方向のサイズ|
|width|int|横方向のサイズ|


## サンプル

```C#
public override void OnLayout()
{
    Spacer(50);
}
```
