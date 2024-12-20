---
title: 'Button'
linkTitle: 'Button'
date: 2024-12-16T00:00:00+09:00
weight: 201
---

`Button`はクリック可能な基本的なインタラクティブ要素です。

```C#
UIHost<UIButton> LayoutBase.Button(string text, Action<UIButton> action, float width = 110f)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|ボタンに表示するテキスト|
|action|Action\<UIButton\>|ボタンを押下した時のアクション|
|width|float|ボタンの幅|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var btn = layout.Button("ボタン１", (b) =>
    {
        Debug.Log("Pressed!");
    });

    return this;
}
```
