﻿---
title: ファイル ストアの復元
TOCTitle: ファイル ストアの復元
ms:assetid: 89916fc6-31d3-4c7f-9eaf-c02584761ef4
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/Hh202180(v=OCS.15)
ms:contentKeyID: 52056638
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# ファイル ストアの復元

 

_**トピックの最終更新日:** 2013-02-18_

Standard Edition のファイル ストアは、通常、Standard Edition サーバー上に配置されています。Enterprise Edition のファイル ストアは、通常、ファイル サーバーまたはクラスター上に配置されています。以下の手順では、ファイル ストアの復元方法を説明します。

## ファイル ストアを復元するには

1.  ファイル ストアに障害が発生した場合は、適切なファイル ストアを $Backup\\ から、ファイル サーバーまたは Standard Edition サーバー上のファイル ストアの場所にコピーし、そのフォルダーを共有します。
    

    > [!IMPORTANT]
    > 復元されたファイル ストアのパスとファイル名は、ファイルを使用するコンポーネントがそのファイルにアクセスできるように、バックアップされたファイル ストアと正確に一致する必要があります。



2.  必要に応じて、ファイル ストアに対するアクセス制御リスト (ACL) を設定します。コマンドラインで、次のように入力します。
    
        Enable-CsTopology
    
    <table>
    <thead>
    <tr class="header">
    <th><img src="images/Gg412781.note(OCS.15).gif" title="note" alt="note" />注:</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td>この手順を実行する必要があるのは、復元のプロセスでほかにトポロジ ビルダーを実行していない場合に限られます。</td>
    </tr>
    </tbody>
    </table>
