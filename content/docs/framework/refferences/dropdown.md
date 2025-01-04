---
title: 'Dropdown'
linkTitle: 'Dropdown'
date: 2024-12-16T00:00:00+09:00
weight: 204
---

ドロップダウン（プルダウン）要素を生成します。


```C#
UIDropdown YKLayout.Dropdown(List<string>? list = null, Action<int>? action = null, int? value = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|list|List<string\>|選択肢のリスト|
|action|Action<int\>|項目を変更する度に呼ばれるアクション|
|value|int|初期インデックス|


## サンプル

```C#
public override void OnLayout()
{
    Dropdown(["選択肢１", "選択肢２"], (idx) => {}, 1);
}
```
