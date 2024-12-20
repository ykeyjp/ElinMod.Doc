---
title: 'InputText'
linkTitle: 'InputText'
date: 2024-12-16T00:00:00+09:00
weight: 200
---

キーボードの入力を受け付けるインタラクティブ要素を生成します。

```C#
UIHost<UIInputText> LayoutBase.InputText(string? value = null, Action<int>? onchange = null, float width = 90f)
```

## 引数
|引数|型|説明|
|--|--|--|
|value|string|初期データ|
|onchange|Action\<UIInputText\>|値が変更される度に呼び出されるアクション|
|width|float|横幅|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    layout.InputText("test", (input) => 
    {
        var txt = input.Text; // string
        var num = input.Num; // int
    });

    return this;
}
```
