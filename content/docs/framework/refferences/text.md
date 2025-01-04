---
title: 'Text'
linkTitle: 'Text'
date: 2024-12-16T00:00:00+09:00
weight: 103
---

装飾されていないテキストを生成します。

```C#
UIText YKLayout.Text(string text, FontColor color = FontColor.DontChange)
UIText YKLayout.TextLong(string text, FontColor color = FontColor.DontChange)
UIText YKLayout.TextMedium(string text, FontColor color = FontColor.DontChange)
UIText YKLayout.TextSmall(string text, FontColor color = FontColor.DontChange)
UIText YKLayout.TextFlavor(string text, FontColor color = FontColor.DontChange)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|テキスト|
|color|FontColor|色|


## サンプル

```C#
public override void OnLayout()
{
    Text("テキスト１");
}
```
