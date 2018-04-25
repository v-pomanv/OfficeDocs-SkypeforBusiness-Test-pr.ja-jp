﻿---
title: 会議参加時間レポート
TOCTitle: 会議参加時間レポート
ms:assetid: e64dc89a-25e4-4cb8-bcb1-51712e69ba5a
ms:mtpsurl: https://technet.microsoft.com/ja-jp/library/JJ205344(v=OCS.15)
ms:contentKeyID: 48273998
ms.date: 05/19/2016
mtps_version: v=OCS.15
ms.translationtype: HT
---

# 会議参加時間レポート

 

_**トピックの最終更新日:** 2015-03-09_

会議参加時間の概要を使用すると、ユーザーが会議に参加するのに要した時間を判定できます。このレポートは、平均参加時間 (ミリ秒) を表示します。また、2 秒以内に会議に参加できたユーザーの数や会議に参加するのに 2 ～ 5 秒かかったユーザーの数などが分かる詳細を提供します。

## 会議参加時間レポートにアクセスする

監視レポートのホーム ページから会議参加時間レポートにアクセスできます。

## フィルター

フィルターは、細かく絞り込んだデータ セットを返したり、返されたデータをさまざま方法で表示したりする方法として利用できます。次の表に、会議参加時間レポートで使用できるフィルターを示します。

### 会議参加時間レポートのフィルター

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>名前</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>開始</strong></p></td>
<td><p>時間範囲の開始日と開始時刻。データを時間単位で表示するには、次のように開始日と開始時刻の両方を入力します。</p>
<p>7/7/2012 1:00 PM</p>
<p>開始時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に開始します。データを日単位で表示するには、次のように日付のみを入力します。</p>
<p>7/7/2012</p>
<p>週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</p>
<p>7/3/2012</p>
<p>週は、常に日曜日から土曜日までです。</p></td>
</tr>
<tr class="even">
<td><p><strong>終了</strong></p></td>
<td><p>時間範囲の終了日と終了時刻。データを時間単位で表示するには、次のように終了日と終了時刻の両方を入力します。</p>
<p>7/7/2012 1:00 PM</p>
<p>終了時刻を入力しないと、レポートは自動的に指定日の午前 12:00 に終了します。データを日単位で表示するには、次のように日付のみを入力します。</p>
<p>7/7/2012</p>
<p>週単位または月単位で表示するには、表示する週または月の任意の日付を入力します (その週または月の最初の日である必要はありません)。</p>
<p>7/3/2012</p>
<p>週は、常に日曜日から土曜日までです。</p></td>
</tr>
<tr class="odd">
<td><p><strong>間隔</strong></p></td>
<td><p>時間間隔です。次のいずれかを選択します。</p>
<ul>
<li><p>時間単位 (最大 25 時間の表示が可能)</p></li>
<li><p>日単位 (最大 31 日の表示が可能)</p></li>
<li><p>週単位 (最大 12 週の表示が可能)</p></li>
<li><p>月単位 (最大 12 か月の表示が可能)</p></li>
</ul>
<p>入力した開始日と終了日が選択した間隔で使用できる値の最大数を超える場合は、最大数の値 (開始日からカウント) のみが表示されます。たとえば、開始日と終了日をそれぞれ 7/7/2012 (2012 年 7 月 7 日)、2/28/2012 (2012 年 2 月 28 日) として毎日の間隔を選択しても、2012 年 8 月 7 日の午前 12:00 から 2012 年 9 月 7 日の午前 12:00 までの日付のデータ (つまり、合計 31 日分のデータのみ) が表示されることになります。</p></td>
</tr>
<tr class="even">
<td><p><strong>プール</strong></p></td>
<td><p>レジストラー プールまたはエッジ サーバーの完全修飾ドメイン名 (FQDN)。個別のプールを選択するか、[<strong>すべて</strong>] をクリックしてすべてのプールのデータを表示できます。このドロップダウン リストは、データベース内のレコードに基づいて自動的に設定されます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>会議セッション</strong></p></td>
<td><p>セッションの種類。有効な値は次のとおりです。</p>
<ul>
<li><p>[すべて]</p></li>
<li><p>フォーカス セッション</p></li>
<li><p>アプリケーション共有</p></li>
<li><p>音声ビデオ会議</p></li>
</ul>
<p>[すべて] を選択した場合は、会議参加時間の合計がレポートの上部に表示されます。これらの合計は、Microsoft Exchange または Microsoft Outlook を使用してスケジュールされた会議のみについての合計であることに注意してください。</p></td>
</tr>
</tbody>
</table>


## 指標

次の表に、会議参加時間レポートで提供される情報を示します。

### 会議参加時間レポートの指標

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>名前</th>
<th>この項目での並べ替え</th>
<th>説明</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>日付</strong></p>
<p>この指標の実際の名前は、選択した間隔によって異なります。</p></td>
<td><p>いいえ</p></td>
<td><p>会議が開催された日時です。</p></td>
</tr>
<tr class="even">
<td><p><strong>セッションの合計数</strong></p></td>
<td><p>いいえ</p></td>
<td><p>セッションの総数です。成功したセッション、失敗したセッション (予期されるエラーと予期しないエラーの両方)、およびどちらにも分類されないセッションを含みます。</p></td>
</tr>
<tr class="odd">
<td><p><strong>平均 (ミリ秒)</strong></p></td>
<td><p>いいえ</p></td>
<td><p>参加者が会議に参加するのに要した平均時間 (ミリ秒) です。</p></td>
</tr>
<tr class="even">
<td><p><strong>セッション &lt; 2 秒、数</strong></p></td>
<td><p>いいえ</p></td>
<td><p>2 秒未満で会議に参加できた参加者の数です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>セッション &lt; 2 秒、割合</strong></p></td>
<td><p>いいえ</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p><strong>セッション 2 ～ 5 秒、数</strong></p></td>
<td><p>いいえ</p></td>
<td><p>2 ～ 5 秒で会議に参加できた参加者の数です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>セッション 2 ～ 5 秒、割合</strong></p></td>
<td><p>いいえ</p></td>
<td><p>2 ～ 5 秒で会議に参加できた参加者の合計の割合です。</p></td>
</tr>
<tr class="even">
<td><p><strong>セッション 5 ～ 10 秒、数</strong></p></td>
<td><p>いいえ</p></td>
<td><p>5 ～ 10 秒で会議に参加できた参加者の数です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>セッション 5 ～ 10 秒、割合</strong></p></td>
<td><p>いいえ</p></td>
<td><p>5 ～ 10 秒で会議に参加できた参加者の合計の割合です。</p></td>
</tr>
<tr class="even">
<td><p><strong>セッション &gt; 10 秒、数</strong></p></td>
<td><p>いいえ</p></td>
<td><p>会議に参加するのに 10 秒以上かかった参加者の数です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>セッション &gt; 10 秒、割合</strong></p></td>
<td><p>いいえ</p></td>
<td><p>会議に参加するのに 10 秒以上かかった参加者の合計の割合です。</p></td>
</tr>
</tbody>
</table>
