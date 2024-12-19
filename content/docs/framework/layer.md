---
title: 'レイヤー（Window）作成'
linkTitle: 'レイヤー作成'
date: 2024-12-16T00:00:00+09:00
weight: 2
---


まず始めにWindow（レイヤー）を定義します。

Winddowに渡したいデータがあれば、`IBuildUIArgs`を継承した構造体にプロパティを定義しておきます。  
例えばキャラクターを参照するようなUIを作る場合には`Chara`をプロパティに含めます。  
アイテムであれば`Thing`をプロパティに含めます。  
ここでは一例ですので空の構造体とします。

```C#
public struct CustomArgs : IBuildUIArgs { }

public class CustomWindow : BuildUI<CustomArgs>
{
    public override BuildUI<CustomArgs> Setup(CustomArgs args)
    {
        var window = this.Window(640, 480, "カスタムウィンドウ");

        return this;
    }
}
```

`BuildUI`を継承したクラスでUIを構築する処理を記述します。`Setup`はその処理を記述するメソッドです。  
引数で`IBuildUIArgs`を経書した構造体が渡されますので、`Chara`や`Thing`の参照はここから取得してください。

上の例で唯一記述されている`this.Window`メソッドはUIのベースとなるウィンドウを生成する命令です。  
定義された内容を箇条書きでまとめると次の通りです。

1. `CustomArgs`と言う構造体を宣言。データは何も持たない。
2. `CustomWindow`と言うウィンドウを宣言。
3. 呼び出し時はサイズ`640x480`のウィンドウが生成される（タイトルはとりあえず`カスタムウィンドウ`）

続いて[UI要素の作成]({{% relref "element.md" %}})セクションでウィンドウに配置するパーツについて学んでみましょう。
