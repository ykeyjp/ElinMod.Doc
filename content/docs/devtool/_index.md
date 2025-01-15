---
title: 'YK DevTool'
linkTitle: 'YK DevTool'
date: 2024-01-04T00:00:00+09:00
weight: 20
sidebar:
    open: true
---

## YK DevToolとは？

Modの開発やさまざまなデータ検証をフォローするツールとして開発されました。  
キャラクターやアイテムのデータを編集したり、レシピ習得やアイテム生成を手助けする機能があります。

[YK Testing Tool](https://steamcommunity.com/sharedfiles/filedetails/?id=3365678112)の後継として開発されたModです。  
`YK Testing Tool`自体もMod開発における実験的Modでした。  
そこで得たノウハウをもとに、UI構成支援Modの[YK Framework](../framework/) と開発支援Modの`YK DevTool`を開発しました。


## Modの導入

次のリンクよりサブスクライブしてElinに`YK DevTool`を導入してください。  
※`YK DevTool`の利用には`YK Framework`も必要です。

{{< cards >}}
  {{< card link="https://steamcommunity.com/sharedfiles/filedetails/?id=3400020753" title="YK Framework on Steam" icon="external-link" >}}
  {{< card link="https://steamcommunity.com/sharedfiles/filedetails/?id=3400020855" title="YK DevTool on Steam" icon="external-link" >}}
{{< /cards >}}


## メニュー

システムメニューやキャラ・アイテムをミドルクリックすると操作メニューが表示されます。

{{< figure src="img/system-menu.png" >}}

### システムメニュー → ツール → 開発ツール

メインウィンドウを表示するメニューです。

### システムメニュー → ツール → レシピツール

レシピ習得状況を編集するメニューです。

### システムメニュー → ツール → アイテム生成ツール

アイテムを生成するツールを表示するメニューです。

## 機能

{{< cards >}}
  {{< card link="./main/" title="Main" image="" subtitle="開発ツール" >}}
  {{< card link="./edit-chara/" title="CharaEdit" image="" subtitle="キャラクターの編集" >}}
  {{< card link="./edit-thing/" title="ThingEdit" image="" subtitle="アイテムの編集" >}}
  {{< card link="./main/" title="BranchEdit" image="" subtitle="拠点の編集" >}}
  {{< card link="./main/" title="Teleport" image="" subtitle="ゾーン移動" >}}
  {{< card link="./recipe-tool/" title="RecipeTool" image="" subtitle="レシピ習得状況の編集" >}}
  {{< card link="./thing-generator/" title="ThingGenerator" image="" subtitle="アイテム生成ツール" >}}
{{< /cards >}}
