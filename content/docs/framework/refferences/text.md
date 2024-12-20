---
title: 'Text'
linkTitle: 'Text'
date: 2024-12-16T00:00:00+09:00
weight: 103
---

装飾されていないテキストを生成します。

```C#
UIHost<UIText> LayoutBase.Text(string text, Action<UIText>? modify = null, float? width = null)
```

## 引数
|引数|型|説明|
|--|--|--|
|text|string|テキスト|
|modify|Action\<UIText\>|UITextの初期化完了前に実行するアクション|
|width|float|横幅|

`modify`パラメーターは`SkinType`や`FontColor`の設定など、要素の初期化が完了する前（`ApplySkin`メソッドが実行される前）に行いたい処理がある場合に使用します。


## サンプル

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");
    var layout = window.Vertial();
    var text = layout.Text("テキスト１");

    return this;
}
```
