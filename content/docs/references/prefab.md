---
title: '内部リソース'
linkTitle: '内部リソース'
date: 2024-12-16T00:00:00+09:00
weight: 1
---

## リソースID
UnityのPrefabに格納されているデータ（いわゆるGameObject）のリソースIDで、
`UnityEngine.Resources.Load`メソッドで呼び出せる文字列形式のキーを収集したリストです。

{{< cards >}}
  {{< card link="" title="（準備中）" icon="link" >}}
{{< /cards >}}

{{< callout type="warning" >}}
  実際に`UnityEngine.Resources.Load("リソースID")`をコールすれば生成されますが、内容や用途を確認していないものも多いので、検証の際は壊れても良いセーブデータで使用してください。  
  オブジェクトを生成するだけで、セーブデータに反映されるような処理はないと思いますが念のため。
{{< /callout >}}

