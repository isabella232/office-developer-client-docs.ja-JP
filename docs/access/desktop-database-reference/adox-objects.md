---
title: ADOX オブジェクト (デスクトップ データベース参照のアクセス)
TOCTitle: ADOX objects
ms:assetid: d7db1aed-251b-888b-bc44-f61caeeac403
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250087(v=office.15)
ms:contentKeyID: 48548018
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: d5051a9842645ac8f93be26bf6309dd05da7ec24
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28704785"
---
# <a name="adox-objects"></a><span data-ttu-id="2bbd2-102">ADOX のオブジェクト</span><span class="sxs-lookup"><span data-stu-id="2bbd2-102">ADOX objects</span></span>

<span data-ttu-id="2bbd2-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="2bbd2-104">各オブジェクトは、対応するコレクションに格納できます。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-104">Each object can be contained in its corresponding collection.</span></span> <span data-ttu-id="2bbd2-105">たとえば、 **Table** オブジェクトは、 [Tables](tables-collection-adox.md) コレクションに格納できます。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-105">For example, a **Table** object can be contained in a [Tables](tables-collection-adox.md) collection.</span></span> <span data-ttu-id="2bbd2-106">詳細については、 [ADOX コレクション](adox-collections.md)」、またはコレクションの特定のトピックを参照してください。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-106">For more information, see [ADOX collections](adox-collections.md) or a specific collection topic.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="2bbd2-107">オブジェクト</span><span class="sxs-lookup"><span data-stu-id="2bbd2-107">Object</span></span></p></th>
<th><p><span data-ttu-id="2bbd2-108">説明</span><span class="sxs-lookup"><span data-stu-id="2bbd2-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2bbd2-109"><a href="catalog-object-adox.md">Catalog</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-109"><a href="catalog-object-adox.md">Catalog</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-110">データ ソースのスキーマ カタログを表すコレクションを含みます。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-110">Contains collections that describe the schema catalog of a data source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bbd2-111"><a href="column-object-adox.md">列</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-111"><a href="column-object-adox.md">Column</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-112">テーブル、インデックス、またはキーの列を表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-112">Represents a column from a table, index, or key.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bbd2-113"><a href="group-object-adox.md">グループ</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-113"><a href="group-object-adox.md">Group</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-114">保護されているデータベースへの権限を持つグループ アカウントを表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-114">Represents a group account that has access permissions within a secured database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bbd2-115"><a href="index-object-adox.md">Index</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-115"><a href="index-object-adox.md">Index</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-116">データベース テーブルのインデックスを表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-116">Represents an index from a database table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bbd2-117"><a href="key-object-adox.md">Key</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-117"><a href="key-object-adox.md">Key</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-118">データベース テーブルの主キー フィールド、外部キー フィールド、または一意なキー フィールドを表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-118">Represents a primary, foreign, or unique key field from a database table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bbd2-119"><a href="procedure-object-adox.md">プロシージャ</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-119"><a href="procedure-object-adox.md">Procedure</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-120">ストアド プロシージャを表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-120">Represents a stored procedure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bbd2-121"><a href="table-object-adox.md">Table</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-121"><a href="table-object-adox.md">Table</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-122">列、インデックス、およびキーを含むデータベース テーブルを表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-122">Represents a database table, including columns, indexes, and keys.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2bbd2-123"><a href="user-object-adox.md">ユーザー</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-123"><a href="user-object-adox.md">User</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-124">保護されているデータベースへの権限を持つユーザー アカウントを表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-124">Represents a user account that has access permissions within a secured database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2bbd2-125"><a href="view-object-adox.md">View</a></span><span class="sxs-lookup"><span data-stu-id="2bbd2-125"><a href="view-object-adox.md">View</a></span></span></p></td>
<td><p><span data-ttu-id="2bbd2-126">抽出されたレコードのセットまたは仮想テーブルを表します。</span><span class="sxs-lookup"><span data-stu-id="2bbd2-126">Represents a filtered set of records or a virtual table.</span></span></p></td>
</tr>
</tbody>
</table>

<br/>



