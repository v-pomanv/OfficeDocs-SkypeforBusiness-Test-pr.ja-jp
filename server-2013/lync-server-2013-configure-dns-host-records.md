﻿---
title: 'Lync Server 2013: DNS ホスト レコードの構成'
TOCTitle: DNS ホスト レコードの構成
ms:assetid: 78a1afcf-41c8-4da5-8740-c6570c19078c
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg398593(v=OCS.15)
ms:contentKeyID: 48272566
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 での DNS ホスト レコードの構成

 

_**トピックの最終更新日:** 2012-10-01_

この手順を適切に完了するには、少なくとも Domain Admins グループのメンバーまたは DnsAdmins グループのメンバーとしてサーバーまたはドメインにログオンする必要があります。

## DNS ホスト A レコードを構成するには

1.  ドメイン ネーム システム (DNS) サーバーで、\[**スタート**\]、\[**管理ツール**\]、および \[**DNS**\] の順にクリックします。

2.  ドメインのコンソール ツリーで、\[**前方参照ゾーン**\] を展開し、Lync Server 2013 がインストールされるドメインを右クリックします。

3.  \[**新しいホスト (A または AAAA)**\] をクリックします。

4.  \[**名前**\] をクリックして、プールのホスト名を入力します (ドメイン名は、レコードが定義されるゾーンから取られるため、A レコードの一部として入力する必要はありません)。

5.  \[**IP アドレス**\] をクリックし、フロント エンド プールのロード バランサーの仮想 IP (VIP) を入力します。
    

    > [!IMPORTANT]
    > ディレクター プールを使用する展開では、簡易 URL のホスト (A) はディレクター ロード バランサーの VIP をポイントする必要があります。

    
    > [!NOTE]
    > ロード バランサーなしでトポロジに接続する Enterprise Edition サーバーまたはディレクターを 1 つだけ展開する場合、または Standard Edition サーバーを展開する場合は、Enterprise Edition サーバー、Standard Edition サーバー、または Director の IP アドレスを入力します。 プールに複数の Enterprise Edition サーバーまたはディレクターを展開する場合は、ロード バランサーが必要です。 ロード バランサーは、Standard Edition サーバーでは使用されません。


6.  \[**ホストの追加**\] をクリックし、\[**OK**\] をクリックします。

7.  追加の A レコードを作成するには、ステップ 4. と 5. を繰り返します。

8.  必要な A レコードをすべて作成したら、\[**完了**\] をクリックします。

