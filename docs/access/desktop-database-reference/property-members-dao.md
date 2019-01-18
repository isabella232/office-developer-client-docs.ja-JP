---
title: プロパティのメンバー (DAO)
TOCTitle: Property Members
ms:assetid: 32658adb-f153-148d-a216-eb97b996579a
ms:mtpsurl: https://msdn.microsoft.com/library/Ff192303(v=office.15)
ms:contentKeyID: 48544076
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: fe60c12a85eff0dd8f796f9affeef71979dac580
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28699143"
---
# <a name="property-members-dao"></a><span data-ttu-id="a78d8-102">プロパティのメンバー (DAO)</span><span class="sxs-lookup"><span data-stu-id="a78d8-102">Property members (DAO)</span></span>


<span data-ttu-id="a78d8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="a78d8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="a78d8-104">Property オブジェクトは、DAO オブジェクトの組み込みまたはユーザー定義の特性を表します。</span><span class="sxs-lookup"><span data-stu-id="a78d8-104">A Property object represents a built-in or user-defined characteristic of a DAO object.</span></span>

## <a name="properties"></a><span data-ttu-id="a78d8-105">Properties</span><span class="sxs-lookup"><span data-stu-id="a78d8-105">Properties</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="a78d8-106">名前</span><span class="sxs-lookup"><span data-stu-id="a78d8-106">Name</span></span></p></th>
<th><p><span data-ttu-id="a78d8-107">説明</span><span class="sxs-lookup"><span data-stu-id="a78d8-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a78d8-108"><strong><a href="property-inherited-property-dao.md">Inherited</a></strong></span><span class="sxs-lookup"><span data-stu-id="a78d8-108"><strong><a href="property-inherited-property-dao.md">Inherited</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a78d8-109">基になるオブジェクトから <strong><a href="property-object-dao.md">Property</a></strong> オブジェクトが継承されるかどうかを示す値を取得します。</span><span class="sxs-lookup"><span data-stu-id="a78d8-109">Returns a value that indicates whether a <strong><a href="property-object-dao.md">Property</a></strong> object is inherited from an underlying object.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78d8-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span><span class="sxs-lookup"><span data-stu-id="a78d8-110"><strong><a href="property-name-property-dao.md">Name</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a78d8-p101">指定したオブジェクトの名前を取得または設定します。オブジェクトがコレクションに追加されていない場合、値の取得および設定が可能です。文字列型 ( <strong>String</strong>) の値を使用します。オブジェクトがコレクションに追加されている場合、値の取得のみ可能です。文字列型 ( <strong>String</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a78d8-p101">Returns or sets the name of the specified object. Read/write <strong>String</strong> if the object has not been appended to a collection. Read-only <strong>String</strong> if the object has been appended to a collection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78d8-114"><strong><a href="property-properties-property-dao.md">Properties</a></strong></span><span class="sxs-lookup"><span data-stu-id="a78d8-114"><strong><a href="property-properties-property-dao.md">Properties</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a78d8-p102">指定したオブジェクトの <strong><a href="properties-collection-dao.md">Properties</a></strong> コレクションを取得します。値の取得のみ可能です。  </span><span class="sxs-lookup"><span data-stu-id="a78d8-p102">Returns the <strong><a href="properties-collection-dao.md">Properties</a></strong> collection of the specified object. Read-only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a78d8-117"><strong><a href="property-type-property-dao.md">型</a></strong></span><span class="sxs-lookup"><span data-stu-id="a78d8-117"><strong><a href="property-type-property-dao.md">Type</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a78d8-p103">オブジェクトの操作の種類またはデータ型を示す値を設定または取得します。値の取得および設定が可能です。整数型 ( <strong>Integer</strong> ) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a78d8-p103">Sets or returns a value that indicates the operational type or data type of an object. Read/write <strong>Integer</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a78d8-120"><strong><a href="property-value-property-dao.md">Value</a></strong></span><span class="sxs-lookup"><span data-stu-id="a78d8-120"><strong><a href="property-value-property-dao.md">Value</a></strong></span></span></p></td>
<td><p><span data-ttu-id="a78d8-p104">オブジェクトの値を設定します。値の取得および設定が可能です。バリアント型 ( <strong>Variant</strong>) の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a78d8-p104">Sets or returns the value of an object. Read/write <strong>Variant</strong>.</span></span></p></td>
</tr>
</tbody>
</table>

