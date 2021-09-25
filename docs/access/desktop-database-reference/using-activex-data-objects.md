---
title: ActiveX データ オブジェクトを使う
TOCTitle: Use ActiveX Data Objects
description: Microsoft Access には、Access データベースとその関連データの作成、管理、管理に使用する 3 つのオブジェクト モデルが用意Visual Basic。
ms:assetid: 64055c45-7a27-2296-468a-015362898329
ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15)
ms:contentKeyID: 48545279
ms.date: 10/16/2018
mtps_version: v=office.15
f1_keywords:
- vbaac10.chm5285627
f1_categories:
- Office.Version=v15
ms.localizationpriority: medium
ms.openlocfilehash: 7f17eb51a0cd1e7dbbafb145d64b2f66716d88f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59588939"
---
# <a name="use-activex-data-objects"></a>ActiveX データ オブジェクトを使う

**適用先**: Access 2013、Office 2013

Microsoft Access には、Access データベースとその関連データの作成、管理、管理に使用する 3 つのオブジェクト モデルが用意Visual Basic。

## <a name="microsoft-activex-data-objects-ado"></a>ADO (ActiveX データ オブジェクト)

ADO には、指定されたデータソースからレコードを作成、保守、および削除するために必要なオブジェクトが含まれてます。

## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Microsoft ADO ext. for DDL and security (ADOX)

ADOX は、セキュリティを管理するために必要なオブジェクトに加えて、新しいデータベースとその格納されているオブジェクトを作成するために必要なデータ定義言語 (DDL) オブジェクトを提供します。

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Microsoft Jet オブジェクトとレプリケーション オブジェクト 2.5 ライブラリ (JRO)

ADO オブジェクトは Microsoft Jet データベースに加えて多くのデータベースで動作するように設計されていたため、Jet 固有の機能が JRO ライブラリに組み込まれています。

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
(MDB のみ)</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Recordsets を作成します。</p></td>
<td><p>X</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>[スタートアップ のプロパティの編集] をクリックします。</p></td>
<td><p>X</p></td>
<td><p>X**</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>ANSI92 SQL.*** をサポートする</p></td>
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
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>既存のテーブル プロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>テーブルリレーションシップを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>セキュリティ設定の編集。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p>X*</p></td>
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
<td><p>保存されている基本的なクエリSQLビューを編集します。</p></td>
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
<td><p>データベースをコンパクト/エンコードします。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<td><p>キャッシュの更新。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X</p></td>
</tr>
<tr class="odd">
<td><p>データベースを複製可能にする。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<td><p>データベース レプリカを作成します。</p></td>
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
<td><p>データベース のプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>カスタム データベース プロパティを作成します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>テーブル列のプロパティを編集します。</p></td>
<td><p>X</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\* Microsoft Access データベースを操作するときのみ使用できます。SQL プロバイダーの将来のバージョンでは、この機能は Microsoft Access プロジェクト (.adp) で提供される可能性があります。

\*\* Access プロジェクトを操作するときのみ使用できます。

\*\*\*Access データベース エンジンは一部の ANSI 92 SQLサポートしますが、まだ ANSI92 に完全に準拠していません。

1 Connection オブジェクト **を使用** してデータベースを参照します。

2 Catalog **オブジェクトを使用** してデータベースを参照します。

3 レプリカ オブジェクト **を使用** してデータベースを参照します。

4 **JetEngine オブジェクトを使用** してデータベースを参照します。


> [!NOTE]
> DAO とは異なり、ADO オブジェクトと ADOX オブジェクトは、それらのデータベースのプロバイダーがアクションをサポートしている限り、Jet 以外のデータベースでマークされたアクションを実行できます。


