---
title: 'Topic'
linkTitle: 'Topic'
date: 2024-12-16T00:00:00+09:00
weight: 102
---

２つのテキストを並べて表示する要素を生成します。
ステータス能力のように名前＋ベース値のように表示される箇所で使用されています。

```C#
UIItem YKLayout.Topic(string text, string? value = null)
UIItem YKLayout.TopicAttribute(string text, string? value = null)
UIItem YKLayout.TopicDomain(string text, string? value = null)
UIItem YKLayout.TopicLeft(string text, string? value = null)
UIItem YKLayout.TopicPair(string text, string? value = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|左側に表示するテキスト|
|value|string|右側に表示するテキスト|


## サンプル

```C#
public override void OnLayout()
{
    layout.Topic("テキスト１", "テキスト２");
}
```
