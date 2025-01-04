---
title: 'Layer'
linkTitle: 'Layer'
date: 2024-12-16T00:00:00+09:00
weight: 1
---

Elinのプログラムにおいて、本来`Layer`と`Window`は別々の機能を持つオブジェクトですが、  
本フレームワークではUIの構築を簡素化するため、`Layer`に１つの`Window`を内包する構成で生成しています。

レイヤーを定義する際にいくつかの上書き可能なオプションがあります。

## サンプル

```C#
public class CustomLayer : YKLayer<Thing>
{
    public override void OnLayout()
    {
        CreateTab<CustomTab>("タブ名"._("Tab Name"), "タブに割り振るID");
    }

    // ウィンドウのデフォルトのタイトル（タブ生成時にタブの名称で置き換えられる）
    public override string Title { get; } = "ウィンドウ"._("Window");

    // ウィンドウのサイズを宣言（デフォルトは 640x480）
    public override Rect Bound { get; } = new Rect(0, 0, 640, 480);
}
```
