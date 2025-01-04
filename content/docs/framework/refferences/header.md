---
title: 'Header'
linkTitle: 'Header'
date: 2024-12-16T00:00:00+09:00
weight: 101
---

装飾されたテキストを生成します。

```C#
UIItem YKLayout.Header(string text, Sprite? sprite = null)
UIItem YKLayout.HeaderCard(string text, Sprite? sprite = null)
UIItem YKLayout.HeaderSmall(string text, Sprite? sprite = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|テキスト|
|sprite|Sprite|テキストの頭に付けるアイコン|


## サンプル

```C#
public override void OnLayout()
{
    Header("ヘッダー１");
}
```
