---
title: Level オブジェクト (ADO MD)
TOCTitle: Level object (ADO MD)
ms:assetid: ddbcabce-8777-1068-98a3-be209084f497
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250121(v=office.15)
ms:contentKeyID: 48548160
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 70fb359aa4faa0bcfc99f0b1700b0eb51f665bc0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32290115"
---
# <a name="level-object-ado-md"></a><span data-ttu-id="36369-102">Level オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="36369-102">Level object (ADO MD)</span></span>


<span data-ttu-id="36369-103">**適用先:** Access 2013、Office 2013</span><span class="sxs-lookup"><span data-stu-id="36369-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="36369-104">階層内で同じランクを持つメンバーのセットが含まれます。</span><span class="sxs-lookup"><span data-stu-id="36369-104">Contains a set of members, each of which has the same rank within a hierarchy.</span></span>

## <a name="remarks"></a><span data-ttu-id="36369-105">注釈</span><span class="sxs-lookup"><span data-stu-id="36369-105">Remarks</span></span>

<span data-ttu-id="36369-106">**Level** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="36369-106">With the collections and properties of a **Level** object, you can do the following:</span></span>

  - <span data-ttu-id="36369-107">**Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Level](uniquename-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="36369-107">Identify the **Level** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="36369-108">**Caption** プロパティを使用して、 [Level](caption-property-ado-md.md) を表示する際に使用する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="36369-108">Return a string to use when displaying the **Level** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="36369-109">**Description** プロパティを使用して、 [Level](description-property-ado-md.md) を表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="36369-109">Return a meaningful string that describes the **Level** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="36369-110">[Members](member-object-ado-md.md) コレクションを使用して、 **Level** を構成する [Member](members-collection-ado-md.md) オブジェクトを返します。</span><span class="sxs-lookup"><span data-stu-id="36369-110">Return the [Member](member-object-ado-md.md) objects that make up the **Level** with the [Members](members-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="36369-111">**Depth** プロパティを使用して、 [Level](depth-property-ado-md.md) のルートからのレベルの数を返します。</span><span class="sxs-lookup"><span data-stu-id="36369-111">Return the number of levels from the root of the **Level** with the [Depth](depth-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="36369-112">標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Level** オブジェクトに関する追加情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="36369-112">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="36369-p101">**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="36369-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="36369-117">名前</span><span class="sxs-lookup"><span data-stu-id="36369-117">Name</span></span></p></th>
<th><p><span data-ttu-id="36369-118">説明</span><span class="sxs-lookup"><span data-stu-id="36369-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="36369-119">CatalogName</span><span class="sxs-lookup"><span data-stu-id="36369-119">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="36369-120">このキューブが属しているカタログの名前。</span><span class="sxs-lookup"><span data-stu-id="36369-120">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36369-121">CubeName</span><span class="sxs-lookup"><span data-stu-id="36369-121">CubeName</span></span></p></td>
<td><p><span data-ttu-id="36369-122">キューブの名前。</span><span class="sxs-lookup"><span data-stu-id="36369-122">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36369-123">説明</span><span class="sxs-lookup"><span data-stu-id="36369-123">Description</span></span></p></td>
<td><p><span data-ttu-id="36369-124">レベルの説明。</span><span class="sxs-lookup"><span data-stu-id="36369-124">A meaningful description of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36369-125">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="36369-125">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="36369-126"><a href="dimension-object-ado-md.md">次元</a>の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="36369-126">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36369-127">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="36369-127">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="36369-128">階層の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="36369-128">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36369-129">levelcaption</span><span class="sxs-lookup"><span data-stu-id="36369-129">LevelCaption</span></span></p></td>
<td><p><span data-ttu-id="36369-130">レベルに関連付けられているラベルまたはキャプション。</span><span class="sxs-lookup"><span data-stu-id="36369-130">A label or caption associated with the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36369-131">levelcardinality</span><span class="sxs-lookup"><span data-stu-id="36369-131">LevelCardinality</span></span></p></td>
<td><p><span data-ttu-id="36369-132">レベルのメンバー数。</span><span class="sxs-lookup"><span data-stu-id="36369-132">The number of members in the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36369-133">levelguid</span><span class="sxs-lookup"><span data-stu-id="36369-133">LevelGUID</span></span></p></td>
<td><p><span data-ttu-id="36369-134">レベルの GUID。</span><span class="sxs-lookup"><span data-stu-id="36369-134">The GUID of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36369-135">LevelName</span><span class="sxs-lookup"><span data-stu-id="36369-135">LevelName</span></span></p></td>
<td><p><span data-ttu-id="36369-136">レベルの名前。</span><span class="sxs-lookup"><span data-stu-id="36369-136">Name of the level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36369-137">levelnumber</span><span class="sxs-lookup"><span data-stu-id="36369-137">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="36369-138">階層のルートとレベルの距離。</span><span class="sxs-lookup"><span data-stu-id="36369-138">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36369-139">leveltype</span><span class="sxs-lookup"><span data-stu-id="36369-139">LevelType</span></span></p></td>
<td><p><span data-ttu-id="36369-140">レベルの種類。</span><span class="sxs-lookup"><span data-stu-id="36369-140">The type of level.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="36369-141">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="36369-141">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="36369-142">レベルの明確な名前。</span><span class="sxs-lookup"><span data-stu-id="36369-142">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="36369-143">SchemaName</span><span class="sxs-lookup"><span data-stu-id="36369-143">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="36369-144">このキューブが属しているスキーマの名前。</span><span class="sxs-lookup"><span data-stu-id="36369-144">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

