---
title: 'Button'
linkTitle: 'Button'
date: 2024-12-16T00:00:00+09:00
weight: 201
---

`Button`はクリック可能な基本的なインタラクティブ要素です。

```C#
UIButton YKLayout.Button(string text, Action action)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|ボタンに表示するテキスト|
|action|Action|ボタンを押下した時のアクション|


## サンプル

```C#
public override void OnLayout()
{
    Button("ボタン１", () =>
    {
        Debug.Log("Pressed!");
    });
}
```
