---
title: 'Dropdown'
linkTitle: 'Dropdown'
date: 2024-12-16T00:00:00+09:00
weight: 204
---

ドロップダウン（プルダウン）要素を生成します。


```C#
UIHost<UIDropdown> LayoutBase.Dropdown()
```

## 引数
|引数|型|説明|
|--|--|--|
|なし|||


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var dropdown = layout.Dropdown();

    // 選択肢追加
    dropdown.Host.AddOptions(["選択肢１", "選択肢２"]);
    // 選択肢クリア
    dropdown.Host.ClearOptions();

    return this;
}
```
