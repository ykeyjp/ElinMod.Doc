---
title: 'Window'
linkTitle: 'Window'
date: 2024-12-16T00:00:00+09:00
weight: 1
---

`Layer`と`Window`はElinのクラスです。YK Frameworkでは`Layer`から`Window`を生成する拡張メソッドを定義しています。

```C#
Window Layer.Window(int width, int height, string caption)
Window Layer.Window(Window.Setting setting)
```

## 引数
|引数|型|説明|
|--|--|--|
|width|int|ウィンドウの幅|
|height|int|ウィンドウの高さ|
|caption|string|ウィンドウのキャプション（タイトル）|
|setting|Window.Setting|Window.Setting構造体を使ってWindowを生成|


## サンプル

YK Frameworkの`BuildUI`クラスは`Layer`を継承しているので、`this.Window()`で`Window`を生成可能です。

```C#
public override BuildUI<CustomArgs> Setup(CustomArgs args)
{
    var window = this.Window(640, 480, "カスタムウィンドウ");

    return this;
}
```
