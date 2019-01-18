---
title: インデックス メンバー (DAO)
TOCTitle: Index Members
ms:assetid: e261c5fa-ca7d-0d63-1c29-48e9231b39d1
ms:mtpsurl: https://msdn.microsoft.com/library/Ff835712(v=office.15)
ms:contentKeyID: 48548290
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 895f29a5dd3e7ed267b96d6a46dc2c8710b4998e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709160"
---
# <a name="index-members-dao"></a><span data-ttu-id="95dd7-102">インデックス メンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="95dd7-102">Index members (DAO)</span></span>


<span data-ttu-id="95dd7-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="95dd7-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="95dd7-p101">Index オブジェクトは、データベース テーブルからアクセスされるレコードの順序、および重複するレコードを受け付けるかどうかを指定して、データに効率的にアクセスできるようにします。外部データベースの場合、Index オブジェクトは、外部キー側のテーブルに対して設定されたインデックスを記述します (Microsoft Access ワークスペースの場合のみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-p101">Index objects specify the order of records accessed from database tables and whether or not duplicate records are accepted, providing efficient access to data. For external databases, Index objects describe the indexes established for external tables (Microsoft Access workspaces only).</span></span>

## <a name="methods"></a><span data-ttu-id="95dd7-106">メソッド</span><span class="sxs-lookup"><span data-stu-id="95dd7-106">Methods</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95dd7-107">名前</span><span class="sxs-lookup"><span data-stu-id="95dd7-107">Name</span></span></p></th>
<th><p><span data-ttu-id="95dd7-108">説明</span><span class="sxs-lookup"><span data-stu-id="95dd7-108">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95dd7-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-109"><strong><a href="index-createfield-method-dao.md">CreateField</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-110">新しい <strong><a href="field-object-dao.md">Field</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-110">Creates a new <strong><a href="field-object-dao.md">Field</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95dd7-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-111"><strong><a href="index-createproperty-method-dao.md">CreateProperty</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-112">新しいユーザー定義の <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトを作成します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-112">Creates a new user-defined <strong><a href="property-object-dao.md">Property</a></strong> object (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="properties"></a><span data-ttu-id="95dd7-113">Properties</span><span class="sxs-lookup"><span data-stu-id="95dd7-113">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="95dd7-114">名前</span><span class="sxs-lookup"><span data-stu-id="95dd7-114">Name</span></span></p></th>
<th><p><span data-ttu-id="95dd7-115">説明</span><span class="sxs-lookup"><span data-stu-id="95dd7-115">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="95dd7-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-116"><strong><a href="index-clustered-property-dao.md">Clustered</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-p102"><strong>Index</strong> オブジェクトがテーブルのクラスター化インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。値の取得および設定が可能です。ブール型 ( <strong>Boolean</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95dd7-p102">Sets or returns a value that indicates whether an <strong>Index</strong> object represents a clustered index for a table (Microsoft Access workspaces only). Read/write <strong>Boolean</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95dd7-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-119"><strong><a href="index-distinctcount-property-dao.md">DistinctCount</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-120">関連付けられたテーブルに含まれる <strong><a href="index-object-dao.md">Index</a></strong> オブジェクトの一意の値の数を示す値を返します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-120">Returns a value that indicates the number of unique values for the <strong><a href="index-object-dao.md">Index</a></strong> object that are included in the associated table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95dd7-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-121"><strong><a href="index-fields-property-dao.md">Fields</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-p103">指定したオブジェクトに格納されているすべての <strong>Field</strong> オブジェクトを表す <strong>Fields</strong> コレクションを取得します。値の取得および設定が可能です。</span><span class="sxs-lookup"><span data-stu-id="95dd7-p103">Returns a <strong>Fields</strong> collection that represents all stored <strong>Field</strong> objects for the specified object. Read/write.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95dd7-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-124"><strong><a href="index-foreign-property-dao.md">Foreign</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-p104"><strong><a href="index-object-dao.md">Index</a></strong> オブジェクトがテーブルの外部キーを表すかどうかを示す値を取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-p104">Returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a foreign key in a table (Microsoft Access workspaces only). .</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95dd7-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-127"><strong><a href="index-ignorenulls-property-dao.md">IgnoreNulls</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-128">インデックス フィールドに Null 値を持つレコードがインデックス エントリを持つかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-128">Sets or returns a value that indicates whether records that have Null values in their index fields have index entries (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95dd7-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-129"><strong><a href="index-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-p105">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="95dd7-p105">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95dd7-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-133"><strong><a href="index-primary-property-dao.md">Primary</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-134"><strong><a href="index-object-dao.md">Index</a></strong> オブジェクトがテーブルの主キー インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-134">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a primary key index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95dd7-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-135"><strong><a href="index-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-p106">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="95dd7-p106">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="95dd7-138"><strong><a href="index-required-property-dao.md">必須</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-138"><strong><a href="index-required-property-dao.md">Required</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-139"><strong><a href="field-object-dao.md">Field</a></strong> オブジェクトに非 Null 値が必要かどうかを示す値を設定または取得します。</span><span class="sxs-lookup"><span data-stu-id="95dd7-139">Sets or returns a value that indicates whether a <strong><a href="field-object-dao.md">Field</a></strong> object requires a non-Null value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="95dd7-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span><span class="sxs-lookup"><span data-stu-id="95dd7-140"><strong><a href="index-unique-property-dao.md">Unique</a></strong></span></span></p></td>
<td><p><span data-ttu-id="95dd7-141"><strong><a href="index-object-dao.md">Index</a></strong> オブジェクトがテーブルの固有 (キー) インデックスを表すかどうかを示す値を設定または取得します (Microsoft Access ワークスペースのみ)。</span><span class="sxs-lookup"><span data-stu-id="95dd7-141">Sets or returns a value that indicates whether an <strong><a href="index-object-dao.md">Index</a></strong> object represents a unique (key) index for a table (Microsoft Access workspaces only).</span></span></p></td>
</tr>
</tbody>
</table>

