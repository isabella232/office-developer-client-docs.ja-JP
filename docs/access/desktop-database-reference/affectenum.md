---
title: AffectEnum (デスクトップ データベース参照のアクセス)
TOCTitle: AffectEnum
ms:assetid: 15393398-d7eb-a685-1bfa-d6712d8e5015
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248916(v=office.15)
ms:contentKeyID: 48543404
ms.date: 10/18/2018
mtps_version: v=office.15
ms.openlocfilehash: 9e1bd4d86e6e269c9363daca0ffa7b8df6303326
ms.sourcegitcommit: 801b1b54786f7b0e5b0d35466e7ae8d1e840b26f
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25863669"
---
# <a name="affectenum"></a><span data-ttu-id="7d7dc-102">AffectEnum</span><span class="sxs-lookup"><span data-stu-id="7d7dc-102">AffectEnum</span></span>

<span data-ttu-id="7d7dc-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="7d7dc-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="7d7dc-104">操作の対象となるレコードを表します。</span><span class="sxs-lookup"><span data-stu-id="7d7dc-104">Specifies which records are affected by an operation.</span></span>

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d7dc-105">定数</span><span class="sxs-lookup"><span data-stu-id="7d7dc-105">Constant</span></span></p></th>
<th><p><span data-ttu-id="7d7dc-106">値</span><span class="sxs-lookup"><span data-stu-id="7d7dc-106">Value</span></span></p></th>
<th><p><span data-ttu-id="7d7dc-107">説明</span><span class="sxs-lookup"><span data-stu-id="7d7dc-107">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d7dc-108"><strong>adAffectAll</strong></span><span class="sxs-lookup"><span data-stu-id="7d7dc-108"><strong>adAffectAll</strong></span></span></p></td>
<td><p><span data-ttu-id="7d7dc-109">3</span><span class="sxs-lookup"><span data-stu-id="7d7dc-109">3</span></span></p></td>
<td><p><span data-ttu-id="7d7dc-110"><strong>Recordset</strong> に適用されている <a href="filter-property-ado.md">Filter</a> がない場合、すべてのレコードが対象です。
</span><span class="sxs-lookup"><span data-stu-id="7d7dc-110">If there is not a <a href="filter-property-ado.md">Filter</a> applied to the <strong>Recordset</strong>, affects all records.</span></span> <span data-ttu-id="7d7dc-111">文字列抽出条件を<strong>Filter</strong>プロパティを設定するかどうか (次のように&quot;作成者 = 'Smith'&quot;)、操作の現在のチャプター内の可視レコードに影響を与えます。</span><span class="sxs-lookup"><span data-stu-id="7d7dc-111">If the <strong>Filter</strong> property is set to a string criteria (such as &quot;Author='Smith'&quot;), the operation affects visible records in the current chapter.</span></span> <span data-ttu-id="7d7dc-112"><strong>Filter</strong>プロパティは、ブックマークの配列または<a href="filtergroupenum.md">FilterGroupEnum</a>のメンバーに設定されて、する場合、操作、<strong>レコード セット</strong>のすべての行に影響します。</span><span class="sxs-lookup"><span data-stu-id="7d7dc-112">If the <strong>Filter</strong> property is set to a member of the <a href="filtergroupenum.md">FilterGroupEnum</a> or an array of Bookmarks, the operation will affect all rows of the <strong>Recordset</strong>.</span></span></p>
<p><span data-ttu-id="7d7dc-113"><strong>注</strong>: adAffectAll は、Visual Basic のオブジェクト ブラウザーで非表示にします。</span><span class="sxs-lookup"><span data-stu-id="7d7dc-113"><strong>NOTE</strong>: adAffectAll is hidden in the Visual Basic Object Browser.</span></span></p>
</td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d7dc-114"><strong>呼び出します</strong></span><span class="sxs-lookup"><span data-stu-id="7d7dc-114"><strong>adAffectAllChapters</strong></span></span></p></td>
<td><p><span data-ttu-id="7d7dc-115">4</span><span class="sxs-lookup"><span data-stu-id="7d7dc-115">4</span></span></p></td>
<td><p><span data-ttu-id="7d7dc-116">現在適用されている <strong>Filter</strong> で非表示になっているレコードを含む、<strong>Recordset</strong> のすべての兄弟チャプターの全レコードに反映されます。</span><span class="sxs-lookup"><span data-stu-id="7d7dc-116">Affects all records in all sibling chapters of the <strong>Recordset</strong>, including those not visible via any <strong>Filter</strong> that is currently applied.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d7dc-117"><strong>adAffectCurrent</strong></span><span class="sxs-lookup"><span data-stu-id="7d7dc-117"><strong>adAffectCurrent</strong></span></span></p></td>
<td><p><span data-ttu-id="7d7dc-118">1</span><span class="sxs-lookup"><span data-stu-id="7d7dc-118">1</span></span></p></td>
<td><p><span data-ttu-id="7d7dc-119">現在のレコードにのみ反映されます。</span><span class="sxs-lookup"><span data-stu-id="7d7dc-119">Affects only the current record.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d7dc-120"><strong>adAffectGroup</strong></span><span class="sxs-lookup"><span data-stu-id="7d7dc-120"><strong>adAffectGroup</strong></span></span></p></td>
<td><p><span data-ttu-id="7d7dc-121">2</span><span class="sxs-lookup"><span data-stu-id="7d7dc-121">2</span></span></p></td>
<td><p><span data-ttu-id="7d7dc-p102">現在の <a href="filter-property-ado.md">Filter</a> プロパティの設定を満たすレコードにのみ反映されます。このオプションを使用するには、<strong>Filter</strong> プロパティを <strong>FilterGroupEnum</strong> 値または <strong>Bookmark</strong> の配列に設定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7d7dc-p102">Affects only records that satisfy the current <a href="filter-property-ado.md">Filter</a> property setting. You must set the <strong>Filter</strong> property to a <strong>FilterGroupEnum</strong> value or an array of <strong>Bookmarks</strong> to use this option.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a><span data-ttu-id="7d7dc-124">ADO/WFC に相当</span><span class="sxs-lookup"><span data-stu-id="7d7dc-124">ADO/WFC equivalent</span></span>

<span data-ttu-id="7d7dc-125">パッケージ: **com.ms.wfc.data**</span><span class="sxs-lookup"><span data-stu-id="7d7dc-125">Package: **com.ms.wfc.data**</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="7d7dc-126">定数</span><span class="sxs-lookup"><span data-stu-id="7d7dc-126">Constant</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7d7dc-127">AdoEnums.Affect.ALL</span><span class="sxs-lookup"><span data-stu-id="7d7dc-127">AdoEnums.Affect.ALL</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d7dc-128">AdoEnums.Affect.ALLCHAPTERS</span><span class="sxs-lookup"><span data-stu-id="7d7dc-128">AdoEnums.Affect.ALLCHAPTERS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7d7dc-129">AdoEnums.Affect.CURRENT</span><span class="sxs-lookup"><span data-stu-id="7d7dc-129">AdoEnums.Affect.CURRENT</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7d7dc-130">AdoEnums.Affect.GROUP</span><span class="sxs-lookup"><span data-stu-id="7d7dc-130">AdoEnums.Affect.GROUP</span></span></p></td>
</tr>
</tbody>
</table>

