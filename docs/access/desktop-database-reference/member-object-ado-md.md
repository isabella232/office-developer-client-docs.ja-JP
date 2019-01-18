---
title: Member オブジェクト (ADO MD)
TOCTitle: Member object (ADO MD)
ms:assetid: d80c024a-07dc-7a35-f8f2-b4d5b19d89e4
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250088(v=office.15)
ms:contentKeyID: 48548025
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 380fdf6c15f6774e27221e8500100870d22350c4
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28709580"
---
# <a name="member-object-ado-md"></a><span data-ttu-id="5399b-102">Member オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="5399b-102">Member object (ADO MD)</span></span>


<span data-ttu-id="5399b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="5399b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="5399b-104">キューブ内のレベルのメンバー、レベルのメンバーの子、またはセルセットの軸に沿ったメンバーの位置を表します。</span><span class="sxs-lookup"><span data-stu-id="5399b-104">Represents a member of a level in a cube, the children of a member of a level, or a member of a position along an axis of a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="5399b-105">解説</span><span class="sxs-lookup"><span data-stu-id="5399b-105">Remarks</span></span>

<span data-ttu-id="5399b-p101">**Member** のプロパティは、使用されているコンテキストによって異なります。 **CubeDef** の [Level](level-object-ado-md.md) の [Member](cubedef-object-ado-md.md) には、階層の現在の [Member](children-property-ado-md.md) のすぐ下のレベルの **Members** を返す **Children** プロパティがあります。 **Position** の [Member](position-object-ado-md.md) では、 **Children** コレクションは常に空です。また、 [Type](type-property-ado-md.md) プロパティは、 **Level** の **Members** のみに適用されます。</span><span class="sxs-lookup"><span data-stu-id="5399b-p101">The properties of a **Member** differ depending on the context in which it is used. A **Member** of a [Level](level-object-ado-md.md) in a [CubeDef](cubedef-object-ado-md.md) has a [Children](children-property-ado-md.md) property that returns the **Members** on the next lower level in the hierarchy from the current **Member**. For a **Member** of a [Position](position-object-ado-md.md), the **Children** collection is always empty. Also, the [Type](type-property-ado-md.md) property applies only to **Members** of a **Level**.</span></span>

<span data-ttu-id="5399b-p102">**Position** の **Member** には、 [Cellset](drilleddown-property-ado-md.md) を表示する際に有用な [DrilledDown](parentsameasprev-property-ado-md.md) プロパティと [ParentSameAsPrev](cellset-object-ado-md.md) プロパティがあります。 **Level** の **Member** でこの 2 つのプロパティにアクセスすると、エラーが発生します。</span><span class="sxs-lookup"><span data-stu-id="5399b-p102">A **Member** of **Position** has two properties — [DrilledDown](drilleddown-property-ado-md.md) and [ParentSameAsPrev](parentsameasprev-property-ado-md.md) — that are useful when displaying the [Cellset](cellset-object-ado-md.md). An error will occur if these properties are accessed on a **Member** of a **Level**.</span></span>

<span data-ttu-id="5399b-112">**Level** の **Member** オブジェクトのコレクションとプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5399b-112">With the collections and properties of a **Member** object of a **Level**, you can do the following:</span></span>

  - <span data-ttu-id="5399b-113">**Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Member](uniquename-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="5399b-113">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="5399b-114">**Caption** プロパティを使用して、 [Member](caption-property-ado-md.md) を表示する際に使用する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5399b-114">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5399b-115">**Description** プロパティを使用して、単位または式の [Member](description-property-ado-md.md) を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5399b-115">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5399b-116">**Type** プロパティを使用して、 [Member](type-property-ado-md.md) の種類を特定します。</span><span class="sxs-lookup"><span data-stu-id="5399b-116">Determine the nature of the **Member** with the [Type](type-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5399b-117">**LevelDepth** プロパティと **LevelName** プロパティを使用して、 [Member](leveldepth-property-ado-md.md) の [Level](levelname-property-ado-md.md) に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5399b-117">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="5399b-118">**Parent** プロパティと [Children](hierarchy-object-ado-md.md) プロパティを使用して、 [Hierarchy](parent-property-ado-md.md) の関連する [Members](children-property-ado-md.md) を取得します。</span><span class="sxs-lookup"><span data-stu-id="5399b-118">Obtain related **Members** in a [Hierarchy](hierarchy-object-ado-md.md) with the [Parent](parent-property-ado-md.md) and [Children](children-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="5399b-119">**ChildCount** プロパティを使用して、 [Member](childcount-property-ado-md.md) の子の数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="5399b-119">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5399b-120">標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Level** オブジェクトに関する追加情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5399b-120">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="5399b-121">**Axis** に沿って **Position** の [Member](axis-object-ado-md.md) オブジェクトのコレクションとプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="5399b-121">With the collections and properties of a **Member** of a **Position** along an [Axis](axis-object-ado-md.md), you can do the following:</span></span>

  - <span data-ttu-id="5399b-122">**Name** プロパティと [UniqueName](name-property-ado-md.md) プロパティを使用して、 [Member](uniquename-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="5399b-122">Identify the **Member** with the [Name](name-property-ado-md.md) and [UniqueName](uniquename-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="5399b-123">**Caption** プロパティを使用して、 [Member](caption-property-ado-md.md) を表示する際に使用する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5399b-123">Return a string to use when displaying the **Member** with the [Caption](caption-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5399b-124">**Description** プロパティを使用して、メジャーまたは式の [Member](description-property-ado-md.md) を説明する文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="5399b-124">Return a meaningful string that describes a measure or formula **Member** with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5399b-125">**LevelDepth** プロパティと **LevelName** プロパティを使用して、 [Member](leveldepth-property-ado-md.md) の [Level](levelname-property-ado-md.md) に関する情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5399b-125">Obtain information about the **Level** of the **Member** with the [LevelDepth](leveldepth-property-ado-md.md) and [LevelName](levelname-property-ado-md.md) properties.</span></span>

  - <span data-ttu-id="5399b-126">**ChildCount** プロパティを使用して、 [Member](childcount-property-ado-md.md) の子の数をカウントします。</span><span class="sxs-lookup"><span data-stu-id="5399b-126">Count the children of a **Member** with the [ChildCount](childcount-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="5399b-127">[DrilledDown](drilleddown-property-ado-md.md) プロパティを使用して、 **Axis** 上のこの **Member** の直下に少なくとも 1 つの子があるかどうかを特定します。</span><span class="sxs-lookup"><span data-stu-id="5399b-127">Use the [DrilledDown](drilleddown-property-ado-md.md) property to determine whether there is at least one child on the **Axis** immediately following this **Member**.</span></span>

  - <span data-ttu-id="5399b-128">[ParentSameAsPrev](parentsameasprev-property-ado-md.md) プロパティを使用して、この **Member** の親が **Member** の直上の親と同じかどうかを特定します。</span><span class="sxs-lookup"><span data-stu-id="5399b-128">Use the [ParentSameAsPrev](parentsameasprev-property-ado-md.md) property to determine whether the parent of this **Member** is the same as the parent of the immediately preceding **Member**.</span></span>

  - <span data-ttu-id="5399b-129">標準の ADO [Properties](properties-collection-ado.md) コレクションを使用して、 **Level** オブジェクトに関する追加情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="5399b-129">Use the standard ADO [Properties](properties-collection-ado.md) collection to obtain additional information about the **Level** object.</span></span>

<span data-ttu-id="5399b-p103">**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="5399b-p103">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="5399b-134">名前</span><span class="sxs-lookup"><span data-stu-id="5399b-134">Name</span></span></p></th>
<th><p><span data-ttu-id="5399b-135">説明</span><span class="sxs-lookup"><span data-stu-id="5399b-135">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5399b-136">カタログ名</span><span class="sxs-lookup"><span data-stu-id="5399b-136">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="5399b-137">このキューブが属しているカタログの名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-137">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-138">ChildrenCardinality</span><span class="sxs-lookup"><span data-stu-id="5399b-138">ChildrenCardinality</span></span></p></td>
<td><p><span data-ttu-id="5399b-139">メンバーの子の数。</span><span class="sxs-lookup"><span data-stu-id="5399b-139">The number of children that the member has.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-140">キューブ名</span><span class="sxs-lookup"><span data-stu-id="5399b-140">CubeName</span></span></p></td>
<td><p><span data-ttu-id="5399b-141">キューブの名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-141">The name of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-142">Description</span><span class="sxs-lookup"><span data-stu-id="5399b-142">Description</span></span></p></td>
<td><p><span data-ttu-id="5399b-143">メンバーの説明。</span><span class="sxs-lookup"><span data-stu-id="5399b-143">A meaningful description of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-144">DimensionUniqueName</span><span class="sxs-lookup"><span data-stu-id="5399b-144">DimensionUniqueName</span></span></p></td>
<td><p><span data-ttu-id="5399b-145"><a href="dimension-object-ado-md.md">次元</a>の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-145">The unambiguous name of the <a href="dimension-object-ado-md.md">dimension</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-146">HierarchyUniqueName</span><span class="sxs-lookup"><span data-stu-id="5399b-146">HierarchyUniqueName</span></span></p></td>
<td><p><span data-ttu-id="5399b-147">階層の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-147">The unambiguous name of the hierarchy.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-148">LevelNumber</span><span class="sxs-lookup"><span data-stu-id="5399b-148">LevelNumber</span></span></p></td>
<td><p><span data-ttu-id="5399b-149">階層のルートとレベルの距離。</span><span class="sxs-lookup"><span data-stu-id="5399b-149">The distance between the level and the root of the hierarchy.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-150">LevelUniqueName</span><span class="sxs-lookup"><span data-stu-id="5399b-150">LevelUniqueName</span></span></p></td>
<td><p><span data-ttu-id="5399b-151">レベルの明確な名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-151">The unambiguous name of the level.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-152">MemberCaption</span><span class="sxs-lookup"><span data-stu-id="5399b-152">MemberCaption</span></span></p></td>
<td><p><span data-ttu-id="5399b-153">メンバーに関連付けられているラベルまたはキャプション。</span><span class="sxs-lookup"><span data-stu-id="5399b-153">A label or caption associated with the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-154">MemberGUID</span><span class="sxs-lookup"><span data-stu-id="5399b-154">MemberGUID</span></span></p></td>
<td><p><span data-ttu-id="5399b-155">メンバーの GUID。</span><span class="sxs-lookup"><span data-stu-id="5399b-155">The GUID of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-156">メンバー名</span><span class="sxs-lookup"><span data-stu-id="5399b-156">MemberName</span></span></p></td>
<td><p><span data-ttu-id="5399b-157">メンバーの名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-157">The name of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-158">MemberOrdinal</span><span class="sxs-lookup"><span data-stu-id="5399b-158">MemberOrdinal</span></span></p></td>
<td><p><span data-ttu-id="5399b-159">メンバーの序数。</span><span class="sxs-lookup"><span data-stu-id="5399b-159">The ordinal number of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-160">MemberType</span><span class="sxs-lookup"><span data-stu-id="5399b-160">MemberType</span></span></p></td>
<td><p><span data-ttu-id="5399b-161">メンバーの種類。</span><span class="sxs-lookup"><span data-stu-id="5399b-161">The type of the member.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-162">MemberUniqueName</span><span class="sxs-lookup"><span data-stu-id="5399b-162">MemberUniqueName</span></span></p></td>
<td><p><span data-ttu-id="5399b-163">メンバーの明確な名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-163">The unambiguous name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-164">ParentCount</span><span class="sxs-lookup"><span data-stu-id="5399b-164">ParentCount</span></span></p></td>
<td><p><span data-ttu-id="5399b-165">このメンバーが持っている親の数。</span><span class="sxs-lookup"><span data-stu-id="5399b-165">The count of the number of parents that this member has.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-166">ParentLevel</span><span class="sxs-lookup"><span data-stu-id="5399b-166">ParentLevel</span></span></p></td>
<td><p><span data-ttu-id="5399b-167">メンバーの親のレベル番号。</span><span class="sxs-lookup"><span data-stu-id="5399b-167">The level number of the member's parent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5399b-168">ParentUniqueName</span><span class="sxs-lookup"><span data-stu-id="5399b-168">ParentUniqueName</span></span></p></td>
<td><p><span data-ttu-id="5399b-169">メンバーの親の明確な名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-169">The unambiguous name of the member's parent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5399b-170">スキーマ名</span><span class="sxs-lookup"><span data-stu-id="5399b-170">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="5399b-171">このキューブが属しているスキーマの名前。</span><span class="sxs-lookup"><span data-stu-id="5399b-171">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
</tbody>
</table>

