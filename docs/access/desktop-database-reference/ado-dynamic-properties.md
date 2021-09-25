---
title: ADO の動的プロパティ
TOCTitle: ADO dynamic properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.localizationpriority: medium
ms.openlocfilehash: 3f6c3692749e0915fc9e26faf55fc948ee1c96ff
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59602963"
---
# <a name="ado-dynamic-properties"></a>ADO の動的プロパティ

**適用先**: Access 2013、Office 2013

動的プロパティは、[Connection](properties-collection-ado.md) オブジェクト、 [Command](connection-object-ado.md) オブジェクト、または [Recordset](command-object-ado.md) オブジェクトの [Properties](recordset-object-ado.md) コレクションに追加できます。これらの動的プロパティのソースは、 [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) などのデータ プロバイダー、または [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) などのサービス プロバイダーです。各動的プロバイダーの詳細については、それぞれのデータ プロバイダーまたはサービス プロバイダーのマニュアルを参照してください。

「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」では、標準 OLE DB プロバイダーの動的プロパティごとに、ADO 名と OLE DB 名を相互参照できます。

次に示す動的プロパティは特に重要で、前のソースでも説明されています。ADO の特別な機能については、次に示す ADO ヘルプ トピックを参照してください。

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>動的プロパティ</th>
<th>説明</th>
</tr>
<tr class="odd">
<td><p><a href="optimize-property-dynamic-ado.md">最適化</a></p></td>
<td><p>このフィールドにインデックスを作成するかどうかを指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="prompt-property-dynamic-ado.md">Prompt</a></p></td>
<td><p>OLE DB プロバイダーから、ユーザーに対して初期化情報を要求するかどうかを指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></p></td>
<td><p><strong>Recordset</strong> オブジェクトの名前を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="resync-command-property-dynamic-ado.md">Resync Command</a></p></td>
<td><p><strong>Unique Table</strong> 動的プロパティに指定されているテーブルのデータを更新するために <strong>Resync</strong> メソッドが発行する、ユーザー指定のコマンド文字列を指定します。</p></td>
</tr>
<tr class="odd">
<td><p><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table、Unique Schema、Unique Catalog</a></p></td>
<td><p><strong>Unique Table</strong> — 更新、挿入、および削除を許可するベース テーブルの名前を指定します。<br/><br/><strong>一意のスキーマ</strong> : テーブルの所有者のスキーマまたは名前を指定します。<br/><br/><strong>一意のカタログ</strong> : テーブルを含むデータベースのカタログまたは名前を指定します。</p></td>
</tr>
<tr class="even">
<td><p><a href="update-resync-property-dynamic-ado.md">Update Resync</a></p></td>
<td><p><strong>UpdateBatch</strong> メソッドの後に暗黙の <strong>Resync</strong> メソッド操作を実行するかどうかを指定し、実行する場合は、その作用範囲を指定します。</p></td>
</tr>
</tbody>
</table>

<br/>

