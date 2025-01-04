---
title: 'InputText'
linkTitle: 'InputText'
date: 2024-12-16T00:00:00+09:00
weight: 200
---

キーボードの入力を受け付けるインタラクティブ要素を生成します。

```C#
UIInputText YKLayout.InputText(string text, Action<int>? onInput = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|value|string|初期データ|
|onchange|Action\<int\>|値が変更される度に呼び出されるアクション|


## サンプル

```C#
public override void OnLayout()
{
    InputText("test", (valueInt) => 
    {
        Debug.Log(valueInt);
    });
}
```
