---
title: 関係メンバー (DAO)
TOCTitle: Relation Members
ms:assetid: 9ee36e7d-3825-1de8-65fb-64bbcada847c
ms:mtpsurl: https://msdn.microsoft.com/library/Ff198338(v=office.15)
ms:contentKeyID: 48546670
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 8d4b1b1a3a06d0605793667f8c9258ea5b6336f5
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25923729"
---
# <a name="relation-members-dao"></a><span data-ttu-id="f4c41-102">関係メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="f4c41-102">Relation members (DAO)</span></span>


<span data-ttu-id="f4c41-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f4c41-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f4c41-104">Relation オブジェクトは、テーブルまたはクエリのフィールド間のリレーションシップを表します (Microsoft Access データベース エンジン データベースのみ)。</span><span class="sxs-lookup"><span data-stu-id="f4c41-104">A Relation object represents a relationship between fields in tables or queries (Microsoft Access database engine databases only).</span></span>

## <a name="methods"></a><span data-ttu-id="f4c41-105">メソッド</span><span class="sxs-lookup"><span data-stu-id="f4c41-105">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4c41-106">名前</span><span class="sxs-lookup"><span data-stu-id="f4c41-106">Name</span></span></p></th>
<th><p><span data-ttu-id="f4c41-107">説明</span><span class="sxs-lookup"><span data-stu-id="f4c41-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4c41-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-108"><strong><a href="relation-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-109">新しい <strong><a href="field-object-dao.md">Field</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="f4c41-109">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="f4c41-110">プロパティ</span><span class="sxs-lookup"><span data-stu-id="f4c41-110">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="f4c41-111">名前</span><span class="sxs-lookup"><span data-stu-id="f4c41-111">Name</span></span></p></th>
<th><p><span data-ttu-id="f4c41-112">説明</span><span class="sxs-lookup"><span data-stu-id="f4c41-112">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f4c41-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-113"><strong><a href="relation-attributes-property-dao.md">Attributes</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-p101"><strong>Relation</strong> オブジェクトの 1 つまたは複数の属性を示す値を設定または取得します。値の取得および設定が可能です。長整数型 ( <strong>Long</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4c41-p101">Sets or returns a value that indicates one or more characteristics of a <strong>Relation</strong> object. Read/write <strong>Long</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c41-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-116"><strong><a href="relation-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-p102">指定されたオブジェクト用に保存されているすべての <strong>Field</strong> オブジェクトを表す <strong>Fields</strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="f4c41-p102">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c41-119"><strong><a href="relation-foreigntable-property-dao.md">外部テーブル</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-119"><strong><a href="relation-foreigntable-property-dao.md">ForeignTable</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-p103">リレーションシップの外部テーブルの名前を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="f4c41-p103">Sets or returns the name of the foreign table in a relationship (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c41-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-122"><strong><a href="relation-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-p104">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4c41-p104">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c41-126"><strong><a href="relation-partialreplica-property-dao.md">必要</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-126"><strong><a href="relation-partialreplica-property-dao.md">PartialReplica</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-p105">フル レプリカから部分レプリカに値を設定するときに、 <strong>Relation</strong> オブジェクトのリレーションシップを考慮する必要があるかどうかを示す値を設定または取得します (Microsoft Access データベース エンジンのデータベースのみ)。値の取得および設定が可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4c41-p105">Sets or returns a value on a <strong>Relation</strong> object indicating whether that relation should be considered when populating a partial replica from a full replica. (Microsoft Access database engine databases only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f4c41-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-130"><strong><a href="relation-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-p106">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="f4c41-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f4c41-133"><strong><a href="relation-table-property-dao.md">テーブル</a></strong></span><span class="sxs-lookup"><span data-stu-id="f4c41-133"><strong><a href="relation-table-property-dao.md">Table</a></strong></span></span></p></td>
<td><p><span data-ttu-id="f4c41-p107"><strong><a href="relation-object-dao.md">Relation</a></strong> オブジェクトの主テーブルの名前を示します。これは、 <strong><a href="connection-name-property-dao.md">TableDef</a></strong> オブジェクトまたは <strong><a href="tabledef-object-dao.md">QueryDef</a></strong> オブジェクトの <strong><a href="querydef-object-dao.md">Name</a></strong> プロパティの設定値と同じである必要があります (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="f4c41-p107">Indicates the name of a <strong><a href="relation-object-dao.md">Relation</a></strong> object's primary table. This should be equal to the <strong><a href="connection-name-property-dao.md">Name</a></strong> property setting of a <strong><a href="tabledef-object-dao.md">TableDef</a></strong> or <strong><a href="querydef-object-dao.md">QueryDef</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

