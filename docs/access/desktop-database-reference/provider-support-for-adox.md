---
title: ADOX のプロバイダー サポート
TOCTitle: Provider support for ADOX
ms:assetid: 32ea3236-d69f-df94-1685-d8791aeb9e0f
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249100(v=office.15)
ms:contentKeyID: 48544091
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: dd41e368a505e6ef3ac40c0cdca343aef5bd45e8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597136"
---
# <a name="provider-support-for-adox"></a>ADOX のプロバイダー サポート


**適用先**: Access 2013、Office 2013

使用している OLE DB データ プロバイダーによっては、ADOX の特定の機能がサポートされていないことがあります。[Microsoft OLE DB Provider for Microsoft Jet](microsoft-ole-db-provider-for-microsoft-jet.md) の場合、ADOX は完全にサポートされています。 [Microsoft OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md)、[Microsoft OLE DB Provider for ODBC](microsoft-ole-db-provider-for-odbc.md)、または [Microsoft OLE DB Provider for Oracle](microsoft-ole-db-provider-for-oracle.md) でサポートされていない機能の一覧を以下に示します。ADOX は、その他の Microsoft OLE DB プロバイダーではサポートされていません。

## <a name="microsoft-ole-db-provider-for-sql-server"></a>Microsoft OLE DB Provider for SQL Server

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクトまたはコレクション</p></th>
<th><p>使用制限</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Catalog</strong> オブジェクト</p></td>
<td><p><strong>Create</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong> コレクション</p></td>
<td><p>オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Views</strong> コレクション</p></td>
<td><p><strong>Views</strong> はサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedures</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Procedure</strong> オブジェクト</p></td>
<td><p><strong>Command</strong> プロパティはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> コレクション</p></td>
<td><p><strong>Users</strong> はサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> コレクション</p></td>
<td><p><strong>Groups</strong> はサポートされません。</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-odbc"></a>Microsoft OLE DB Provider for ODBC

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクトまたはコレクション</p></th>
<th><p>使用制限</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Catalog</strong> オブジェクト</p></td>
<td><p><strong>Create</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。 オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Procedures</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure</strong> オブジェクト</p></td>
<td><p><strong>Command</strong> プロパティはサポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Indexes</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> コレクション</p></td>
<td><p><strong>Users</strong> はサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> コレクション</p></td>
<td><p><strong>Groups</strong> はサポートされません。</p></td>
</tr>
</tbody>
</table>


## <a name="microsoft-ole-db-provider-for-oracle"></a>Microsoft OLE DB Provider for Oracle

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>オブジェクトまたはコレクション</p></th>
<th><p>使用制限</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Catalog</strong> オブジェクト</p></td>
<td><p><strong>Create</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Tables</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。 オブジェクトの作成前はプロパティ値の取得および設定が可能で、既存のオプジェクトを参照する場合は値の取得のみ可能です。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Views</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>View</strong> オブジェクト</p></td>
<td><p><strong>Command</strong> プロパティはサポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Procedures</strong> オブジェクト</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Procedure</strong> オブジェクト</p></td>
<td><p><strong>Command</strong> プロパティはサポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Indexes</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Keys</strong> コレクション</p></td>
<td><p><strong>Append</strong> メソッドおよび <strong>Delete</strong> メソッドはサポートされません。</p></td>
</tr>
<tr class="odd">
<td><p><strong>Users</strong> コレクション</p></td>
<td><p><strong>Users</strong> はサポートされません。</p></td>
</tr>
<tr class="even">
<td><p><strong>Groups</strong> コレクション</p></td>
<td><p><strong>Groups</strong> はサポートされません。</p></td>
</tr>
</tbody>
</table>

