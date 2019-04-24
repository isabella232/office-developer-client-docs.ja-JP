---
title: ActiveX データ オブジェクトを使う
TOCTitle: Use ActiveX Data Objects
description: Microsoft access では、Visual Basic を使用して access データベースとその関連データを作成、保守、および管理するための3つのオブジェクトモデルを使用できます。
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
localization_priority: Normal
ms.openlocfilehash: 3b530db43a816e66b9fbef254984142aadf0b841
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32312741"
---
# <a name="use-activex-data-objects"></a>ActiveX データ オブジェクトを使う

**適用先:** Access 2013、Office 2013

Microsoft access では、Visual Basic を使用して access データベースとその関連データを作成、保守、および管理するための3つのオブジェクトモデルを使用できます。

## <a name="microsoft-activex-data-objects-ado"></a>ADO (ActiveX データ オブジェクト)

ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>DDL およびセキュリティのための Microsoft ADO ext (ADOX)

ADOX には、セキュリティを管理するために必要なオブジェクトに加えて、新しいデータベースおよびその中に含まれるオブジェクトを作成するために必要なデータ定義言語 (DDL) オブジェクトが用意されています。

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet および Replication オブジェクト2.5 ライブラリ (JRO)

ADO オブジェクトは Microsoft Jet データベースに加えて多くのデータベースで動作するように設計されているため、jet 固有の機能が JRO ライブラリに分割されています。

次の表は、各機能を DAO と比較したものです。

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>機能</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
(mdb のみ)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>レコードセットを作成します。</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>スタートアッププロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p>X * *</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ANSI92 SQL. * * * をサポートします。</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>テーブルを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>新しいデータベースを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>エックス</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>既存の表のプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>テーブルのリレーションシップを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>エックス</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>セキュリティ設定を編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>エックス</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>列データの圧縮属性のサポート。</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>保存された基本的な SQL クエリまたはビューを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>エックス</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>コードでのみアクセス可能なパーマネント クエリの作成</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>エックス</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>コンテナー/UI およびコードでアクセス可能なクエリの作成</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>データベースの最適化/エンコードを行います。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>キャッシュを更新します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>データベースをレプリケート可能にします。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>データベースのレプリカを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>レプリカを同期します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>データベースのプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>カスタムデータベースプロパティを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>テーブルの列のプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。

\*\* Access プロジェクトを操作するときのみ使用できます。

\*\*\*Access データベースエンジンはいくつかの ANSI 92 SQL をサポートしていますが、完全に ANSI92 に準拠しているわけではありません。

1は**Connection**オブジェクトを使用してデータベースを参照します。

2は、 **Catalog**オブジェクトを使用してデータベースを参照します。

3データベースを参照するのには、 **Replica**オブジェクトを使用します。

4 **JetEngine**オブジェクトを使用してデータベースを参照します。


> [!NOTE]
> DAO とは異なり、ADO および ADOX オブジェクトは、Jet 以外のデータベースでマークされたアクションを実行できます。これらのデータベースのプロバイダーがそのアクションをサポートしている場合に限ります。


