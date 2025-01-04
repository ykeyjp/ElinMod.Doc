---
title: 'レイヤー（Window）作成'
linkTitle: 'レイヤー作成'
date: 2024-12-16T00:00:00+09:00
weight: 2
---

まず始めにWindow（レイヤー）を定義します。

レイヤーの生成時にオブジェクトを引数で渡すことができます。  
例えばキャラクターを参照するようなUIを作る場合には`Chara`をプロパティに含めます。  
アイテムであれば`Thing`をプロパティに含めます。

```C#
public class CustomLayer : YKLayer<Thing>
{
    public override void OnLayout()
    {
        CreateTab<CustomTab>("タブ名"._("Tab Name"), "タブに割り振るID");
        // 複数のタブが必要な場合は続けて宣言
        CreateTab<Custom2Tab>("タブ名2"._("Tab Name2"), "タブに割り振るID2");
    }
}
```

タブの宣言もレイヤーと似た構成のクラスとなります。
```C#
public class CustomTab : YKLayout<Thing>
{
    public override void OnLayout()
    {
        // UIの宣言
        // レイヤー生成時に渡されるオブジェクトは this.Layer.Data で取得できます。
        Thing thing = Layer.Data;
    }
}
```

`YKLayout`を継承したクラスでUIを構築する処理を記述します。`OnLayout`はその処理を記述するメソッドです。

定義したレイヤーは次のコードで呼び出すことができます。

```C#
YK.CreateLayer<CustomLayer>(thing);
```

オブジェクトの参照が必要なければ次のような呼び出しも可能です。  
この場合レイヤーの宣言時は `object` を割り当ててください。

```C#
public class CustomLayer : YKLayer<object> {}

YK.CreateLayer<CustomLayer>();
```

ここまでで定義された内容を箇条書きでまとめると次の通りです。

1. `CustomLayer`と言うレイヤーを宣言。
2. `CustomTab`と言うタブを宣言。
3. `YK.CreateLayer`メソッドで定義したレイヤーの生成を命令。
4. サイズ`640x480`のウィンドウが生成される。

続いて[UI要素の作成]({{% relref "element.md" %}})セクションでウィンドウに配置するパーツについて学んでみましょう。
