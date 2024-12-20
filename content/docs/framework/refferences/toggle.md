---
title: 'Toggle'
linkTitle: 'Toggle'
date: 2024-12-16T00:00:00+09:00
weight: 203
---

ON/OFFを切り替えるインタラクティブ要素を生成します。

```C#
UIHost<UIButton> LayoutBase.Toggle(string text, Action<bool> toggle, bool isOn = false)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|トグルに添えるテキスト|
|toggle|Action\<bool\>|ON/OFFが切り替わる度に呼ばれるアクション|
|isOn|bool|初期状態|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var toggle = layout.Toggle("トグル１", (b) =>
    {
        Debug.Log(b);
    }, true);

    return this;
}
```
