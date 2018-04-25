﻿---
title: 'Lync Server 2013: 応答グループのエージェント グループの作成'
TOCTitle: 応答グループのエージェント グループの作成
ms:assetid: 2a80de17-ead0-46e8-8a27-7a4e233dbde0
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Gg520969(v=OCS.15)
ms:contentKeyID: 48271532
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 での応答グループのエージェント グループの作成

 

_**トピックの最終更新日:** 2012-09-12_

エージェント グループを作成するときは、そのグループに割り当てるエージェントを選択し、詳細なグループ設定 (ルーティング方法、グループに対するエージェントの権限など) を指定します。

Lync Server へのサインイン/サインアウトとは別に、グループにサインイン/サインアウトする必要があるエージェントを*公式エージェント*と呼びます。公式エージェントが、グループにルーティングされた着信を受信するには、そのグループにサインインする必要があります。これは、パートタイム ベースでグループから通話に応答するエージェントには便利な方法です。公式エージェントは、Lync 2013 でメニュー項目をクリックして Windows Internet Explorer インターネット ブラウザーを起動し Web ページ コンソールを表示して、グループにサインイン/サインアウトします。

グループにサインインもサインアウトもしていないエージェントを、*非公式エージェント*と呼びます。非公式エージェントは、Lync Server にサインインすると、自動的にそのグループにサインインします。また、非公式エージェントはグループからサインアウトすることはできません。

<table>
<thead>
<tr class="header">
<th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>エージェントにできるのは社内ユーザーのみです。エージェントが社内からオンラインに移動された場合、応答グループの通話はそのエージェントにルーティングされません。</td>
</tr>
</tbody>
</table>


## このセクション中

[Lync Server 2013 エージェント グループの作成または変更](lync-server-2013-create-or-modify-an-agent-group.md)
