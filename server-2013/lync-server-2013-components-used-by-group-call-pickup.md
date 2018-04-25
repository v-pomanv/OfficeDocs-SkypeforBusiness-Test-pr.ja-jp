﻿---
title: グループ通話ピックアップで使用されるコンポーネント
TOCTitle: グループ通話ピックアップで使用されるコンポーネント
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ945625(v=OCS.15)
ms:contentKeyID: 52056581
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# グループ通話ピックアップで使用されるコンポーネント

 

_**トピックの最終更新日:** 2013-01-30_

グループ通話ピックアップは、エンタープライズ VoIP およびコール パーク アプリケーションを展開するときに自動的に展開されます。グループ通話ピックアップを有効にするには、通話ピックアップ グループ番号として指定された個別の番号の範囲を使用してコール パーク オービット テーブルを構成し、ユーザーを通話ピックアップ グループに割り当てて、グループ通話ピックアップに対してユーザーを有効にします。グループ通話ピックアップをサポートする Lync Server コンポーネントは次のとおりです。

  - **アプリケーション サービス**   アプリケーション サービスは、コール パーク アプリケーションなどの統合コミュニケーション アプリケーションを展開、ホスト、および管理するためのプラットフォームです。アプリケーション サービスは、フロント エンド プールのすべてのフロント エンド サーバー、およびすべての Standard Edition サーバーに自動的にインストールされます。

  - **コール パーク アプリケーション**   コール パーク アプリケーションは、アプリケーション サービスがホストする統合通信アプリケーションの 1 つです。グループ通話ピックアップはコール パーク アプリケーションに基づきます。

  - **Lync Server 管理シェル**   Lync Server 管理シェルを使用して、グループ通話ピックアップ グループを管理します。

  - **SEFAUtil リソース キット ツール**   SEFAUtil (セカンダリ拡張機能アクティブ化ユーティリティ) を使用して、ユーザーを通話ピックアップ グループに割り当てて、ユーザーの通話ピックアップを有効または無効にします。
