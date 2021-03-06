﻿---
title: 'Lync Server 2013: 監視要件の定義'
TOCTitle: 組織の監視要件の定義
ms:assetid: d587ff04-9af6-4ac1-ad42-076e7a40ac75
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ205284(v=OCS.15)
ms:contentKeyID: 48273697
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# Lync Server 2013 での監視要件の定義

 

_**トピックの最終更新日:** 2012-09-05_

Microsoft Lync Server 2013 による監視の展開とインストールを効率化すると、組織の監視要件の定義に関連するプロセスも効率化されます。とはいえ、 Lync Server 2013 のインストールと構成を開始する前に対応しなければならないいくつかの重要な問題があります。

**監視するデータの種類。** Lync Server 2013 を使用すると、通話詳細記録 (CDR) データと QoE (Quality of Experience) データという異なる 2 種類のデータを監視できます。通話詳細記録 (CDR) では、ボイス オーバー IP (VoIP) 電話の通話、インスタント メッセージング (IM)、ファイル転送、音声ビデオ (A/V) 会議、アプリケーション共有セッションなどの Lync Server 機能の使用状況を追跡できます。この情報は、使用されている Lync Server 機能 (および使用されていない機能) の特定に役立つとともに、これらの機能が使用されるタイミングに関する情報も提供します。QoE (Quality of Experience) データでは、損失ネットワーク パケット数、背景ノイズ、および "ジッター" の大きさ (パケット遅延の差) など、組織で行われる音声通話やビデオ通話の品質記録を保持することができます。

Lync Server 2013 による監視の有効化を選択した場合は、CDR 監視と QoE 監視の両方を有効にするか、一方の監視タイプを無効にして、もう一方の監視タイプを有効にすることができます。たとえば、ユーザーがインスタント メッセージングとファイル転送だけを使用し、音声またはビデオ通話を行わないとします。この場合、QoE 監視を有効にする意味はほとんどありません。同様に、 Lync Server は、監視を展開した後の監視の有効化と無効化を容易にします。たとえば、監視を展開するが、最初は QoE 監視を無効にする場合があります。ユーザーが音声またはビデオ通話の問題に遭遇し始めた場合は、QoE 監視を有効にし、そのデータを使用してトラブルシューティングとそれらの問題の解決を行います。

Lync Server をインストールした後に監視をインストールすることに較べて、 Lync Server をインストールすると同時に監視をインストールすることに特定の利点 (または短所) はありません。注意する必用がある点は、監視をインストールする前に、バックエンドの監視ストアをホストするコンピューターを選択し、そのコンピューターを監視に使用する前に、サポートされているバージョンの SQL Server をそのコンピューターにインストールして構成する必用があるということです。SQL Server をコンピューターに既にインストールしていて、そのコンピューターを使用する準備ができている場合は、 Lync Server をインストールすると同時に監視をインストールすることができます。バックエンド コンピューターの準備ができていない場合は、 Lync Server を単独でインストールしてから、バックエンド コンピューターを使用する準備ができたときに監視をインストールすることができます。

**監視をインストールするタイミング。**Lync Server 2013 をインストールして構成すると同時に、監視をインストールして構成することができます。Lync Server 展開ウィザードを使用すると、セットアップ中にフロントエンド プールを監視データベースに関連付けることができます。または、Lync Server を単独でインストールした後、監視をインストールできます。トポロジ ビルダーを使用して、フロントエンド プールおよびサーバーを監視データベースに関連付け、変更後のトポロジを公開することによって、これを実行できます。

**必要なバックエンド監視データベースの数。** 単一の監視データベースによって、何万人ものユーザー ( Microsoft Lync Server 2010 の場合、監視およびアーカイブ用の併置データベースが 240,000 人のユーザーをサポートすると見積もられています) をサポートできます。さらに、単一の監視データベースは、複数のフロントエンド プールによって使用されます。組織に 3 つのフロントエンド プールがある場合は、これらの 3 つのプールすべてを同じバックエンド ストアに関連付けることができます。

これは単に、多くの組織では、必要なバックエンド監視データベースの数を決定するときに、データベースの容量が決定的要素にならないということです。その代わり、ネットワークの速度がより重要な考慮事項になります。フロントエンド プールが 3 つあるが、そのうちの 1 つのプールが低速のネットワーク接続に配置されているとします。この場合、2 つの監視データベースを使用することをお勧めします。つまり、1 つのデータベースを良好なネットワーク接続を持つ 2 つのプールに使用し、もう一方のデータベースを低速のネットワーク接続を持つプールに使用します。

監視インフラストラクチャの計画では、 Lync Server 2013 によるミラー データベース使用のサポートも考慮する必要があります。「データベース ミラーリング」を使用すると、データベースの 2 つのコピーを、それぞれ別のサーバー上で同時に保持することができます。データがプライマリ データベースに書き込まれるたびに、同じデータがミラー データベースに書き込まれます。プリマリ データベースに障害が発生した場合、またはプリマリ データベースが使用不能になった場合は、簡単な Lync Server PowerShell コマンドを使用して、ミラー データベースに「フェールオーバー」することができます。次に例を示します。

    Invoke-CsDatabaseFailover -PoolFqdn atl-cs-001.litwareinc.com -DatabaseType "Monitoring" -NewPrincipal "Mirror"

これが重要なのは、ミラーリングでは、必要なデータベースの数が 2 倍になるからです。

**独自のカスタム監視構成が必要な Lync Server サイト。**Lync Server 2013 をインストールするときに、CDR および QoE 構成設定のグローバル コレクションもインストールします。これらのグローバル コレクションを使用して、同じ CDR および QoE 設定を組織全体に適用することができます。すべてのユーザーに対して CDR 監視を有効にする場合など、多くの場合はこれで十分です。

ただし、異なる設定を異なるサイトに適用する必用がある場合もあります。たとえば、Redmond サイトで CDR 監視と QoE 監視の両方を使用するが、Dublin では、CDR 監視だけを使用する場合があります。同様に、Redmond サイトで監視データを 60 日間保持するが、Dublin サイトでは、このタイプのデータを 30 日間だけ保持する必用がある場合があります。 Lync Server 2013を使用すると、サイト スコープで CDR構成設定および QoE 構成設定のそれぞれ別個のコレクションを作成できます (これには、監視の有効化と無効化に加えて、データを保持する期間など、管理設定の構成が含まれます)。

監視を展開する前、または監視を展開した後、これを決定できることに注意してください。たとえば、監視を展開してから、グローバル設定を使用して組織全体を管理できます。後で変更する場合には、たとえば、Redmond サイト用の設定の別個のコレクションを作成し、これらの設定を使用して Redmond 用の監視を管理します (サイト スコープに適用された設定は、グローバル スコープに適用された設定よりも常に優先されます)。再び変更する場合は、Redmond サイトに適用された構成設定を単に削除します。サイト設定のコレクションを削除すると、設定のグローバル コレクションがそのサイトに自動的に適用されます。

