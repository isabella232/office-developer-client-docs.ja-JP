---
title: Hierarchy オブジェクト (ADO MD)
TOCTitle: Hierarchy Object (ADO MD)
ms:assetid: 26e4e690-59ad-fb87-66b0-f3310df42d0c
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249031(v=office.15)
ms:contentKeyID: 48543825
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 34513e3188653bdba04add376f06911ce86386bd
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25479122"
---
# <a name="hierarchy-object-ado-md"></a><span data-ttu-id="317a2-102">Hierarchy オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="317a2-102">Hierarchy Object (ADO MD)</span></span>


<span data-ttu-id="317a2-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="317a2-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="317a2-p101">[次元](dimension-object-ado-md.md)のメンバーを集約または "まとめる" ための 1 つの方法です。次元は 1 つ以上の階層ごとに集約できます。</span><span class="sxs-lookup"><span data-stu-id="317a2-p101">Represents one way in which the members of a [dimension](dimension-object-ado-md.md) can be aggregated or "rolled up." A dimension can be aggregated along one or more hierarchies.</span></span>

## <a name="remarks"></a><span data-ttu-id="317a2-106">解説</span><span class="sxs-lookup"><span data-stu-id="317a2-106">Remarks</span></span>

<span data-ttu-id="317a2-107">**Hierarchy** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="317a2-107">With the collections and properties of a **Hierarchy** object, you can do the following:</span></span>

  - <span data-ttu-id="317a2-108">**Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Hierarchy](uniquename-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="317a2-108">Identify the **Hierarchy** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="317a2-109">**Description** プロパティを使用して、 [Hierarchy](description-property-ado-md.md) を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="317a2-109">Return a meaningful string that describes the **Hierarchy** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="317a2-110">[Levels](level-object-ado-md.md) コレクションを使用して、 **Hierarchy** を構成する [Level](levels-collection-ado-md.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="317a2-110">Return the [Level](level-object-ado-md.md) objects that make up the **Hierarchy** with the [Levels](levels-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="317a2-111">標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Hierarchy** オブジェクトに関する追加情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="317a2-111">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Hierarchy** object.</span></span>

<span data-ttu-id="317a2-p102">**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="317a2-p102">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="317a2-116">名前</span><span class="sxs-lookup"><span data-stu-id="317a2-116">Name</span></span></p></th>
<th><p><span data-ttu-id="317a2-117">説明</span><span class="sxs-lookup"><span data-stu-id="317a2-117">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="317a2-118">AllMember</span><span class="sxs-lookup"><span data-stu-id="317a2-118">AllMember</span></span></p></td>
<td><p><span data-ttu-id="317a2-119">最高レベルのロールアップにおける階層のメンバー。</span><span class="sxs-lookup"><span data-stu-id="317a2-119">The member at the highest level of rollup in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="317a2-120">カタログ名</span><span class="sxs-lookup"><span data-stu-id="317a2-120">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="317a2-121">このキューブが属しているカタログの名前。</span><span class="sxs-lookup"><span data-stu-id="317a2-121">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="317a2-122">キューブ名</span><span class="sxs-lookup"><span data-stu-id="317a2-122">CubeName</span></span></p></td>
<td><p><span data-ttu-id="317a2-123">キューブの名前。</span><span class="sxs-lookup"><span data-stu-id="317a2-123">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="317a2-124">できるよ</span><span class="sxs-lookup"><span data-stu-id="317a2-124">DefaultMember</span></span></p></td>
<td><p><span data-ttu-id="317a2-125">この階層の既定のメンバーの固有の名前。</span><span class="sxs-lookup"><span data-stu-id="317a2-125">The unique name of the default member for this hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="317a2-126">Description</span><span class="sxs-lookup"><span data-stu-id="317a2-126">Description</span></span></p></td>
<td><p><span data-ttu-id="317a2-127">階層の説明。</span><span class="sxs-lookup"><span data-stu-id="317a2-127">A meaningful description of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="317a2-128">DimensionType</span><span class="sxs-lookup"><span data-stu-id="317a2-128">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="317a2-129">この階層が属している次元の種類。</span><span class="sxs-lookup"><span data-stu-id="317a2-129">The type of dimension to which this hierarchy belongs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="317a2-130">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="317a2-130">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="317a2-131">次元の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="317a2-131">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="317a2-132">HierarchyCaption</span><span class="sxs-lookup"><span data-stu-id="317a2-132">HierarchyCaption</span></span></p></td>
<td><p><span data-ttu-id="317a2-133">階層に関連付けられているラベルまたはキャプション。</span><span class="sxs-lookup"><span data-stu-id="317a2-133">A label or caption associated with the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="317a2-134">HierarchyCardinality</span><span class="sxs-lookup"><span data-stu-id="317a2-134">HierarchyCardinality</span></span></p></td>
<td><p><span data-ttu-id="317a2-135">階層のメンバー数。</span><span class="sxs-lookup"><span data-stu-id="317a2-135">The number of members in the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="317a2-136">HierarchyGUID</span><span class="sxs-lookup"><span data-stu-id="317a2-136">HierarchyGUID</span></span></p></td>
<td><p><span data-ttu-id="317a2-137">階層の GUID。</span><span class="sxs-lookup"><span data-stu-id="317a2-137">The GUID of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="317a2-138">HierarchyName</span><span class="sxs-lookup"><span data-stu-id="317a2-138">HierarchyName</span></span></p></td>
<td><p><span data-ttu-id="317a2-139">階層の名前。</span><span class="sxs-lookup"><span data-stu-id="317a2-139">The name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="317a2-140">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="317a2-140">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="317a2-141">階層の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="317a2-141">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="317a2-142">スキーマ名</span><span class="sxs-lookup"><span data-stu-id="317a2-142">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="317a2-143">このキューブが属しているスキーマの名前。</span><span class="sxs-lookup"><span data-stu-id="317a2-143">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

