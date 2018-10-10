---
title: ActiveX データ オブジェクトを使用する
TOCTitle: Using ActiveX Data Objects
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 09/18/2015
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.openlocfilehash: 1f7c57ca785e115e9278145921bf50e8afe870ab
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477335"
---
# <a name="using-activex-data-objects"></a>ActiveX データ オブジェクトを使用する


**適用されます**Access 2013 |。Office 2013

Microsoft Access では、Visual Basic を使って Access データベースとその関連データを作成、保守、および管理するための 3 つの新しいオブジェクト モデルが提供されています。

## <a name="microsoft-activex-data-objects-ado"></a>ADO (ActiveX データ オブジェクト)

ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>ADOX (ADO Ext. for DDL and Security)

ADOX では、セキュリティ管理に必要なオブジェクトのほか、新しいデータベースに必要な DDL (データ定義言語) オブジェクト、およびそれに含まれるオブジェクトが提供されています。

**JRO (Jet and Replication Objects 2.5 Library)**

ADO オブジェクトは、Jet データベースだけでなく、数多くのデータベースと共に動作するよう設計されています。JRO ライブラリには Jet 特有の機能を集めています。

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
(MDB ののみ)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>レコードセットの作成</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>起動時の設定関連のプロパティの編集</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ANSI92 SQL のサポート ***</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>テーブルの作成</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>新しいデータベース</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>既存のテーブルのプロパティの編集</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>テーブルのリレーションシップの作成</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>セキュリティ設定値の編集</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>列データの圧縮属性のサポート</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>格納された基本 SQL クエリまたはビューの編集</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>コードでのみアクセス可能なパーマネント クエリの作成</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X*</p></td>
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
<td><p>データベースの最適化/エンコード</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>キャッシュの更新</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>データベースをレプリケート可能にする</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>データベース レプリカの作成</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<td><p>レプリカの同期をとる</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>データベース プロパティの編集</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>カスタム データベース プロパティの作成</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>列のプロパティの編集</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。

\*\* Access プロジェクトを操作するときのみ使用できます。

\*\*\* Access データベース エンジンは、ANSI 92 SQL のいくつかをサポートしていますが、ANSI92 完全対応ではありません。

1データベースの参照には、 **Connection** オブジェクトを使用します。

2データベースの参照には、 **Catalog** オブジェクトを使用します。

3データベースの参照には、 **Replica** オブジェクトを使用します。

4データベースの参照には、 **JetEngine** オブジェクトを使用します。


> [!NOTE]
> <P>DAO とは異なり、ADO および ADOX オブジェクトは、上記の印がついている動作を Jet ではなく、データベースで実行できます。ただし、使用するデータベースのプロバイダーが、それらの動作をサポートしている場合に限ります。</P>


