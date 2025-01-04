---
title: 'Toggle'
linkTitle: 'Toggle'
date: 2024-12-16T00:00:00+09:00
weight: 203
---

ON/OFFを切り替えるインタラクティブ要素を生成します。

```C#
UIButton YKLayout.Toggle(string text, bool isOn = false, Action<bool>? onClick = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|トグルに添えるテキスト|
|isOn|bool|初期状態|
|toggle|Action\<bool\>|ON/OFFが切り替わる度に呼ばれるアクション|


## サンプル

```C#
public override void OnLayout()
{
    Toggle("トグル１", (b) =>
    {
        Debug.Log(b);
    }, true);
}
```
