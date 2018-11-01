---
title: ADOX の列挙定数
TOCTitle: ADOX Enumerated Constants
ms:assetid: 0ad716a0-8801-50cb-024a-85c308c65c78
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248840(v=office.15)
ms:contentKeyID: 48543163
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 0f8be72ea28d9814890bcaf193c1175725fcfe1d
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25869500"
---
# <a name="adox-enumerated-constants"></a><span data-ttu-id="d01f9-102">ADOX の列挙定数</span><span class="sxs-lookup"><span data-stu-id="d01f9-102">ADOX Enumerated Constants</span></span>


<span data-ttu-id="d01f9-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d01f9-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d01f9-p101">ここでは、デバッグ用に各定数の値の一覧を示します。ただし、この値は参考用のものであり、ADOX のリリースごとに変更されることがあります。コードを記述するときは、列挙定数の実際の値ではなく、名前のみを使って記述するようにしてください。</span><span class="sxs-lookup"><span data-stu-id="d01f9-p101">To assist debugging, the ADOX enumerated constants list a value for each constant. However, this value is purely advisory, and may change from one release of ADOX to another. Your code should only depend on the name, not the actual value, of enumerated constants.</span></span>

<span data-ttu-id="d01f9-107">次の列挙定数が定義されています。</span><span class="sxs-lookup"><span data-stu-id="d01f9-107">The following enumerated constants are defined.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="d01f9-108">列挙</span><span class="sxs-lookup"><span data-stu-id="d01f9-108">Enumeration</span></span></p></th>
<th><p><span data-ttu-id="d01f9-109">説明</span><span class="sxs-lookup"><span data-stu-id="d01f9-109">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d01f9-110"><a href="actionenum.md">ActionEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-110"><a href="actionenum.md">ActionEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-111"><strong>SetPermissions</strong> メソッドの呼び出し時に実行されるアクションの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-111">Specifies the type of action to be performed when <strong>SetPermissions</strong> is called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d01f9-112"><a href="allownullsenum.md">AllowNullsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-112"><a href="allownullsenum.md">AllowNullsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-113">Null 値を含むレコードにインデックスを付けるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-113">Specifies whether records with null values are indexed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d01f9-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-114"><a href="columnattributesenum.md">ColumnAttributesEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-115"><strong>Column</strong> の属性を示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-115">Specifies characteristics of a <strong>Column</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d01f9-116"><a href="datatypeenum.md">DataTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-116"><a href="datatypeenum.md">DataTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-117"><strong>Field</strong>、<strong>Parameter</strong>、または <strong>Property</strong> のデータ型を指定します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-117">Specifies the data type of a <strong>Field</strong>, <strong>Parameter</strong>, or <strong>Property</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d01f9-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-118"><a href="inherittypeenum.md">InheritTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-119"><strong>SetPermissions</strong> メソッドで設定された権限をオブジェクトが継承する方法を示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-119">Specifies how objects will inherit permissions set with <strong>SetPermissions</strong>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d01f9-120"><a href="keytypeenum.md">KeyTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-120"><a href="keytypeenum.md">KeyTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-121"><strong>Key</strong> の種類として、主キー、外部キー、一意なキーのいずれかを示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-121">Specifies the type of <strong>Key</strong>: primary, foreign, or unique.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d01f9-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-122"><a href="objecttypeenum.md">ObjectTypeEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-123">権限または所有権を設定するデータベース オブジェクトの種類を示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-123">Specifies the type of database object for which to set permissions or ownership.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d01f9-124"><a href="rightsenum.md">RightsEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-124"><a href="rightsenum.md">RightsEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-125">オブジェクトに対するグループまたはユーザーの権限を指定します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-125">Specifies the rights or permissions for a group or user on an object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d01f9-126"><a href="ruleenum.md">RuleEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-126"><a href="ruleenum.md">RuleEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-127"><strong>Key</strong> が削除されたときに従うルールを示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-127">Specifies the rule to follow when a <strong>Key</strong> is deleted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d01f9-128"><a href="sortorderenum.md">SortOrderEnum</a></span><span class="sxs-lookup"><span data-stu-id="d01f9-128"><a href="sortorderenum.md">SortOrderEnum</a></span></span></p></td>
<td><p><span data-ttu-id="d01f9-129">インデックスを持つ列の並べ替え順序を示します。</span><span class="sxs-lookup"><span data-stu-id="d01f9-129">Specifies the sort sequence for an indexed column.</span></span></p></td>
</tr>
</tbody>
</table>

