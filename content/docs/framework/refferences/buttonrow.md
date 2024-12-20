---
title: 'ButtonRow'
linkTitle: 'ButtonRow'
date: 2024-12-16T00:00:00+09:00
weight: 202
---

`ButtonRow`はボタンを並べるレイアウトを生成します。  
ボタンは`AddButton`で生成します。  
ボタンのみ並べるレイアウトの場合に適します。

```C#
LayoutButtons LayoutBase.ButtonRow()
UIHost<UIButton> LayoutButtons.AddButton(string text, Action<UIButton> action, float width = 110f)
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
    var buttons = layout.ButtonRow();
    buttons.AddButton("ボタン１", () => 
    {
        Debug.Log("Pressed! (1)");
    });
    buttons.AddButton("ボタン２", () => 
    {
        Debug.Log("Pressed! (2)");
    });

    return this;
}
```
