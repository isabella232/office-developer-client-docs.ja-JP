---
title: ADO の動的プロパティ
TOCTitle: ADO Dynamic Properties
ms:assetid: a908bc52-2cb0-89c7-a997-2cde93477e4d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249782(v=office.15)
ms:contentKeyID: 48546915
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4a953157e7b38aab7989b4c52f60bfffd1c56766
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477954"
---
# <a name="ado-dynamic-properties"></a><span data-ttu-id="e8971-102">ADO の動的プロパティ</span><span class="sxs-lookup"><span data-stu-id="e8971-102">ADO Dynamic Properties</span></span>


<span data-ttu-id="e8971-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e8971-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e8971-p101">動的プロパティは、[Connection](properties-collection-ado.md) オブジェクト、 [Command](connection-object-ado.md) オブジェクト、または [Recordset](command-object-ado.md) オブジェクトの [Properties](recordset-object-ado.md) コレクションに追加できます。これらの動的プロパティのソースは、 [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md) などのデータ プロバイダー、または [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md) などのサービス プロバイダーです。各動的プロバイダーの詳細については、それぞれのデータ プロバイダーまたはサービス プロバイダーのマニュアルを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8971-p101">Dynamic properties can be added to the [Properties](properties-collection-ado.md) collections of the [Connection](connection-object-ado.md), [Command](command-object-ado.md), or [Recordset](recordset-object-ado.md) objects. The source for these properties is either a data provider, such as the [OLE DB Provider for SQL Server](microsoft-ole-db-provider-for-sql-server.md), or a service provider, such as the [Microsoft Cursor Service for OLE DB](microsoft-cursor-service-for-ole-db-ado-service-component.md). Refer to the appropriate data provider or service provider documentation for more information about a specific dynamic property.</span></span>

<span data-ttu-id="e8971-107">「[ADO の動的プロパティ インデックス](ado-dynamic-property-index.md)」では、標準 OLE DB プロバイダーの動的プロパティごとに、ADO 名と OLE DB 名を相互参照できます。</span><span class="sxs-lookup"><span data-stu-id="e8971-107">The [ADO Dynamic Property Index](ado-dynamic-property-index.md) provides a cross-reference between the ADO and OLE DB names for each standard OLE DB provider dynamic property.</span></span>

<span data-ttu-id="e8971-p102">次に示す動的プロパティは特に重要で、前のソースでも説明されています。ADO の特別な機能については、次に示す ADO ヘルプ トピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="e8971-p102">The following dynamic properties are of special interest, and are also documented in the sources mentioned above. Special functionality with ADO is documented in the ADO help topics listed below.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8971-110"><a href="optimize-property-dynamic-ado.md">最適化</a></span><span class="sxs-lookup"><span data-stu-id="e8971-110"><a href="optimize-property-dynamic-ado.md">Optimize</a></span></span></p></td>
<td><p><span data-ttu-id="e8971-111">このフィールドにインデックスを作成するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-111">Specifies whether an index should be created on this field.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8971-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span><span class="sxs-lookup"><span data-stu-id="e8971-112"><a href="prompt-property-dynamic-ado.md">Prompt</a></span></span></p></td>
<td><p><span data-ttu-id="e8971-113">OLE DB プロバイダーから、ユーザーに対して初期化情報を要求するかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-113">Specifies whether the OLE DB provider should prompt the user for initialization information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8971-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span><span class="sxs-lookup"><span data-stu-id="e8971-114"><a href="reshape-name-property-dynamic-ado.md">Reshape Name</a></span></span></p></td>
<td><p><span data-ttu-id="e8971-115"><strong>Recordset</strong> オブジェクトの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-115">Specifies a name for the <strong>Recordset</strong> object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8971-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span><span class="sxs-lookup"><span data-stu-id="e8971-116"><a href="resync-command-property-dynamic-ado.md">Resync Command</a></span></span></p></td>
<td><p><span data-ttu-id="e8971-117"><strong>Unique Table</strong> 動的プロパティに指定されているテーブルのデータを更新するために <strong>Resync</strong> メソッドが発行する、ユーザー指定のコマンド文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-117">Specifies a user-supplied command string that the <strong>Resync</strong> method issues to refresh the data in the table named in the <strong>Unique Table</strong> dynamic property.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8971-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">固有のテーブル、一意のスキーマ、一意なカタログ</a></span><span class="sxs-lookup"><span data-stu-id="e8971-118"><a href="unique-table-unique-schema-unique-catalog-properties-dynamic-ado.md">Unique Table, Unique Schema, Unique Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="e8971-119"><strong>固有のテーブル</strong>更新、挿入、および削除を許可しているベース テーブルの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-119"><strong>Unique Table</strong> — specifies the name of the base table upon which updates, insertions, and deletions are allowed.</span></span> <span data-ttu-id="e8971-120"><strong>一意のスキーマ</strong>スキーマ、またはテーブルの所有者の名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-120"><strong>Unique Schema</strong> — specifies the schema, or name of the owner of the table.</span></span> <span data-ttu-id="e8971-121"><strong>一意なカタログ</strong>カタログ、またはテーブルを含むデータベースの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-121"><strong>Unique Catalog</strong> — specifies the catalog, or name of the database containing the table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8971-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span><span class="sxs-lookup"><span data-stu-id="e8971-122"><a href="update-resync-property-dynamic-ado.md">Update Resync</a></span></span></p></td>
<td><p><span data-ttu-id="e8971-123"><strong>UpdateBatch</strong> メソッドの後に暗黙の <strong>Resync</strong> メソッド操作を実行するかどうかを指定し、実行する場合は、その作用範囲を指定します。</span><span class="sxs-lookup"><span data-stu-id="e8971-123">Specifies whether the <strong>UpdateBatch</strong> method is followed by an implicit <strong>Resync</strong> method operation, and if so, the scope of that operation.</span></span></p></td>
</tr>
</tbody>
</table>

