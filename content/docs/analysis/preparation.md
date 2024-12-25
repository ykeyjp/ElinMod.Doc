---
title: '準備'
linkTitle: '準備'
date: 2024-12-16T00:00:00+09:00
weight: 1
---

ElinなどのUnity製のゲームの解析には`Unity Explorer`が大変便利です。  
ElinではワークショップのModで簡単に導入できるようです。

{{< cards >}}
  {{< card link="https://steamcommunity.com/sharedfiles/filedetails/?id=3364902496" title="Unity Explorer by Elin Mod" icon="external-link" >}}
{{< /cards >}}

ここではオリジナルの`Unity Explorer`を導入する手順を記します。


## パッケージをダウンロード

{{< cards >}}
  {{< card link="https://github.com/yukieiji/UnityExplorer" title="github:yukieiji/UnityExplorer" icon="external-link" >}}
{{< /cards >}}

GitHubのレポジトリを訪れ、Releasesから最新のパッケージをダウンロードします。  
対象は`UnityExplorer.BepInEx6.Mono.zip`です。  
間違えやすいものに`UnityExplorer.BepInEx6.Unity.Mono.zip`がありますが、こちらは今回使用しませんのでご注意ください。


## BepInExのpluginsにコピー

ZIPファイルの内容物を所定のフォルダーにコピーします。

Elinのインストール先のBepInExフォルダーに移動してください。  
Windowsでは以下のフォルダーです。
```
C:\Program Files (x86)\Steam\steamapps\common\Elin\BepInEx
```

ZIPファイルの内容物を次の構成になるようにコピーしてください。

{{< filetree/container >}}
  {{< filetree/folder name="BepInEx" >}}
    {{< filetree/folder name="plugins" >}}
      {{< filetree/folder name="sinai-dev-UnityExplorer" >}}
        {{< filetree/file name="UnityExplorer.BIE6.Mono.dll" >}}
        {{< filetree/file name="UniverseLib.Mono.dll" >}}
      {{< /filetree/folder >}}
    {{< /filetree/folder >}}
  {{< /filetree/folder >}}
{{< /filetree/container >}}

これだけで導入は完了です。  
ゲーム起動中に`F7`キー（初期設定）で`Unity Explorer`を起動できます。


## そのほかの解析用ツール

{{< cards >}}
  {{< card link="https://github.com/icsharpcode/ILSpy" title="ILSpy" icon="external-link" >}}
  {{< card link="https://github.com/dnSpy/dnSpy" title="dnSpy" icon="external-link" >}}
{{< /cards >}}

どちらもC#のアセンブリを解析するのに役立つツールです。  
メンテナンスが続いているILSpyがオススメです。  
Elinのインストールフォルダーにある`Elin_Data\Managed\Elin.dll`を起点に読み込むと良いでしょう。
