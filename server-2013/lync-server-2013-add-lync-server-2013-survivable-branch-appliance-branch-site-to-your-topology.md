﻿---
title: 'Lync Server 2013: トポロジへの Lync Server 2013 存続可能ブランチ アプライアンスのブランチ サイトの追加'
TOCTitle: トポロジへの Lync Server 2013 存続可能ブランチ アプライアンスのブランチ サイトの追加
ms:assetid: d3142a37-4606-456d-8ea9-6cc0e51e55f3
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ721896(v=OCS.15)
ms:contentKeyID: 49887161
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# トポロジへの Lync Server 2013 存続可能ブランチ アプライアンスのブランチ サイトの追加

 

_**トピックの最終更新日:** 2012-10-07_

Microsoft Lync Server 2013存続可能ブランチ アプライアンス (SBA) はバックアップ レジストラーとして Microsoft Lync Server 2010フロント エンド プールに関連付けることはできません。SBA は Microsoft Lync Server 2013フロント エンド プールに関連付ける必要があります。以下の手順は Microsoft Lync Server 2013 SBA を想定しています。セントラル サイトでこの手順を実行します。

## Microsoft Lync Server 2013 を含むブランチ サイトをトポロジに追加するには

1.  トポロジ ビルダーを以下の手順で起動します。\[**スタート**\]、\[**すべてのプログラム**\]、\[**Microsoft Lync Server 2013**\]、\[**Lync Server トポロジ ビルダー**\] の順にクリックします。

2.  コンソール ツリーでセントラル サイトを展開し、\[**ブランチ サイト**\] を展開し、\[**新しいブランチ サイト**\] をクリックします。

3.  \[**新しいブランチ サイトの定義**\] ダイアログ ボックスで、\[**名前**\] をクリックし、新しいブランチ サイトの名前を入力します。

4.  (オプション) \[**説明**\] をクリックし、ブランチ サイトの分かりやすい説明を入力します。

5.  その後、\[**次へ**\] をクリックします。

6.  (オプション) 次の \[**新しいブランチ サイトの定義**\] ダイアログ ボックスで、以下のいずれかの操作を行います。
    
      - \[**市区町村**\] をクリックし、ブランチ サイトが所在する市区町村の名前を入力します。
    
      - \[**都道府県/地域**\] をクリックし、ブランチ サイトが所在する都道府県または地域の名前を入力します。
    
      - \[**国番号**\] をクリックし、ブランチ サイトが所在する国または地域の 2 桁番号を入力します。

7.  \[**次へ**\] をクリックし、次のいずれかを実行します。
    
      - このサイトで 存続可能ブランチ アプライアンスまたは 存続可能ブランチ サーバーを使用している場合は、\[**このウィザードが閉じたら新しい存続可能ウィザードを開く**\] チェック ボックスがオンになっていることを確認します。
    
      - このサイトで 存続可能ブランチ アプライアンスまたは 存続可能ブランチ サーバーを使用していない場合は、\[**このウィザードが閉じたら新しい存続可能ウィザードを開**\] チェック ボックスをクリアします。
    
      - \[**完了**\] をクリックし、その後は、開かれたウィザードの指示に従います。ウィザードの項目の詳細については、「[Lync Server 2013 での存続可能ブランチ アプライアンスまたは存続可能ブランチ サーバーの定義](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)」を参照してください。

8.  トポロジに追加する各ブランチ サイトに対して、前のステップを繰り返します。

## 関連項目

#### タスク

[Lync Server 2013 での存続可能ブランチ アプライアンスまたは存続可能ブランチ サーバーの定義](lync-server-2013-define-a-survivable-branch-appliance-or-server.md)  
[Lync Server 2013 でのブランチ サイト用の PSTN ゲートウェイの定義](lync-server-2013-define-a-pstn-gateway-for-a-branch-site.md)  
[Lync Server 2013 でメディア バイパスを有効にしてトランクを構成する](lync-server-2013-configure-a-trunk-with-media-bypass.md)  
[Lync Server 2013 でメディア バイパスを無効にしてトランクを構成する](lync-server-2013-configure-a-trunk-without-media-bypass.md)

