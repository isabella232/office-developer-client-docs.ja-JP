---
title: Dimension オブジェクト (ADO MD)
TOCTitle: Dimension object (ADO MD)
ms:assetid: 12f43cfc-c74e-a2e8-7f6e-75fc68472c4b
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248902(v=office.15)
ms:contentKeyID: 48543355
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: afea442aa535660b5bb618297640db8fbd546dec
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28712828"
---
# <a name="dimension-object-ado-md"></a><span data-ttu-id="5e4c8-102">Dimension オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="5e4c8-102">Dimension object (ADO MD)</span></span>


<span data-ttu-id="5e4c8-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5e4c8-104">1 つ以上のメンバーの階層を含む、多次元キューブの次元の 1 つを表します。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-104">Represents one of the dimensions of a multidimensional cube, containing one or more hierarchies of members.</span></span>

## <a name="remarks"></a><span data-ttu-id="5e4c8-105">解説</span><span class="sxs-lookup"><span data-stu-id="5e4c8-105">Remarks</span></span>

<span data-ttu-id="5e4c8-106">**Dimension** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-106">With the collections and properties of a **Dimension** object, you can do the following:</span></span>

  - <span data-ttu-id="5e4c8-107">**Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Dimension](uniquename-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-107">Identify the **Dimension** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="5e4c8-108">**Description** プロパティを使用して、 [Dimension](description-property-ado-md.md) を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-108">Return a meaningful string that describes the **Dimension** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5e4c8-109">[Hierarchies](hierarchy-object-ado-md.md) コレクションを使用して、 **Dimension** を構成する [Hierarchy](hierarchies-collection-ado-md.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-109">Return the [Hierarchy](hierarchy-object-ado-md.md) objects that make up the **Dimension** with the [Hierarchies](hierarchies-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="5e4c8-110">標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Dimension** オブジェクトに関する追加情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-110">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Dimension** object.</span></span>

<span data-ttu-id="5e4c8-p101">**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5e4c8-115">名前</span><span class="sxs-lookup"><span data-stu-id="5e4c8-115">Name</span></span></p></th>
<th><p><span data-ttu-id="5e4c8-116">説明</span><span class="sxs-lookup"><span data-stu-id="5e4c8-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5e4c8-117">カタログ名</span><span class="sxs-lookup"><span data-stu-id="5e4c8-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-118">このキューブが属しているカタログの名前。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e4c8-119">キューブ名</span><span class="sxs-lookup"><span data-stu-id="5e4c8-119">CubeName</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-120">キューブの名前。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-120">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e4c8-121">DefaultHierarchy</span><span class="sxs-lookup"><span data-stu-id="5e4c8-121">DefaultHierarchy</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-122">既定の階層の固有の名前。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-122">The unique name of the default hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e4c8-123">Description</span><span class="sxs-lookup"><span data-stu-id="5e4c8-123">Description</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-124">キューブの説明。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-124">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e4c8-125">DimensionCaption</span><span class="sxs-lookup"><span data-stu-id="5e4c8-125">DimensionCaption</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-126">次元に関連付けられているラベルまたはキャプション。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-126">A label or caption associated with the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e4c8-127">DimensionCardinality</span><span class="sxs-lookup"><span data-stu-id="5e4c8-127">DimensionCardinality</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-128">次元のメンバー数。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-128">The number of members in the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e4c8-129">DimensionGUID</span><span class="sxs-lookup"><span data-stu-id="5e4c8-129">DimensionGUID</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-130">次元の GUID。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-130">The GUID of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e4c8-131">DimensionName</span><span class="sxs-lookup"><span data-stu-id="5e4c8-131">DimensionName</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-132">次元の名前。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-132">The name of the dimension.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e4c8-133">DimensionOrdinal</span><span class="sxs-lookup"><span data-stu-id="5e4c8-133">DimensionOrdinal</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-134">キューブを構成する次元のグループ内の次元の序数。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-134">The ordinal number of the dimension among the group of dimensions that form the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e4c8-135">DimensionType</span><span class="sxs-lookup"><span data-stu-id="5e4c8-135">DimensionType</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-136">次元の種類。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-136">The dimension type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5e4c8-137">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="5e4c8-137">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-138">次元の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-138">The unambiguous name of the dimension.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5e4c8-139">スキーマ名</span><span class="sxs-lookup"><span data-stu-id="5e4c8-139">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="5e4c8-140">このキューブが属しているスキーマの名前。</span><span class="sxs-lookup"><span data-stu-id="5e4c8-140">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

