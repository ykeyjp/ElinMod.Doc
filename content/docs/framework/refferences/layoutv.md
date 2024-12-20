---
title: 'LayoutV'
linkTitle: 'Vertical'
date: 2024-12-16T00:00:00+09:00
weight: 2
---

要素を縦に積み上げる（ぶら下げる？）レイアウトを生成します。  
LayoutVはLayoutBaseを継承しているので、ほかの要素を子要素として生成できます。  
生成した順番に並ぶので処理の順序に注意してください。

```C#
LayoutV Window.Vertical()
LayoutBase Window.Tab(string title)
LayoutV LayoutBase.Vertical(float? size = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|title|string|タブのタイトル|
|size|float|固定する場合のサイズ（幅と高さのどちらが対象かは親要素次第）|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var vertical = window.Vertical();

    return this;
}
```

`Window.Tab()`メソッドはウィンドウにタブを付けてページ切り替え機能を提供します。  
返り値は`LayoutV`なので標準は縦に積み上げるレイアウトになります。

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var tab1 = window.Tab("タブ１");
    var tab2 = window.Tab("タブ２");

    return this;
}
```
