---
title: 'Slider'
linkTitle: 'Slider'
date: 2024-12-16T00:00:00+09:00
weight: 205
---

`Dropdown`の亜種でスライダー表現で選択を行うインタラクティブ要素を生成します。

```C#
UIHost<UISlider> LayoutBase.Slider<TValue>(int index, IList<TValue> list, Action<int, TValue> onChange, Func<TValue, string>? getInfo = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|index|int|初期インデックス|
|list|IList\<TValue\>|選択肢のリスト|
|onChange|Action\<int, TValue\>|選択が変化する度に呼ばれるアクション|
|getInfo|Func\<TValue, string\>|リストのデータから表示するテキストを返す関数|


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var slider = layout.Slider(0, new List<string> { "選択肢１", "選択肢２", "選択肢３" }, (idx, str) =>
    {
        Debug.Log(str);
    }, (str) => str);

    return this;
}
```
