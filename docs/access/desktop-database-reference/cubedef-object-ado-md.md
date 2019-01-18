---
title: CubeDef オブジェクト (ADO MD)
TOCTitle: CubeDef object (ADO MD)
ms:assetid: 199235b7-3d98-f655-27bc-94f66e994e06
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248941(v=office.15)
ms:contentKeyID: 48543502
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: c82c95a430da76694fe26300e877e86f86a2eb4b
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28719905"
---
# <a name="cubedef-object-ado-md"></a><span data-ttu-id="4715b-102">CubeDef オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4715b-102">CubeDef object (ADO MD)</span></span>


<span data-ttu-id="4715b-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4715b-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4715b-104">関連する次元のセットを含む、多次元スキーマからのキューブを表します。</span><span class="sxs-lookup"><span data-stu-id="4715b-104">Represents a cube from a multidimensional schema, containing a set of related dimensions.</span></span>

## <a name="remarks"></a><span data-ttu-id="4715b-105">解説</span><span class="sxs-lookup"><span data-stu-id="4715b-105">Remarks</span></span>

<span data-ttu-id="4715b-106">**CubeDef** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="4715b-106">With the collections and properties of a **CubeDef** object, you can do the following:</span></span>

  - <span data-ttu-id="4715b-107">**Name** プロパティを使用して、 [CubeDef](name-property-ado-md.md) を識別します。</span><span class="sxs-lookup"><span data-stu-id="4715b-107">Identify a **CubeDef** with the [Name](name-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="4715b-108">[Description](description-property-ado-md.md) プロパティを使用して、キューブを表す文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="4715b-108">Return a string that describes the cube with the [Description](description-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="4715b-109">[Dimensions](dimensions-collection-ado-md.md) コレクションを使用して、キューブを構成する次元を返します。</span><span class="sxs-lookup"><span data-stu-id="4715b-109">Return the dimensions that make up the cube with the [Dimensions](dimensions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="4715b-110">標準の ADO **Properties** コレクションを使用して、 [CubeDef](properties-collection-ado.md) に関する追加情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="4715b-110">Obtain additional information about the **CubeDef** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="4715b-p101">**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="4715b-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="4715b-115">名前</span><span class="sxs-lookup"><span data-stu-id="4715b-115">Name</span></span></p></th>
<th><p><span data-ttu-id="4715b-116">説明</span><span class="sxs-lookup"><span data-stu-id="4715b-116">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4715b-117">カタログ名</span><span class="sxs-lookup"><span data-stu-id="4715b-117">CatalogName</span></span></p></td>
<td><p><span data-ttu-id="4715b-118">このキューブが属しているカタログの名前。</span><span class="sxs-lookup"><span data-stu-id="4715b-118">The name of the catalog to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4715b-119">CreatedOn</span><span class="sxs-lookup"><span data-stu-id="4715b-119">CreatedOn</span></span></p></td>
<td><p><span data-ttu-id="4715b-120">キューブの作成日時。</span><span class="sxs-lookup"><span data-stu-id="4715b-120">Date and time of cube creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4715b-121">CubeGUID</span><span class="sxs-lookup"><span data-stu-id="4715b-121">CubeGUID</span></span></p></td>
<td><p><span data-ttu-id="4715b-122">キューブの GUID。</span><span class="sxs-lookup"><span data-stu-id="4715b-122">Cube GUID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4715b-123">キューブ名</span><span class="sxs-lookup"><span data-stu-id="4715b-123">CubeName</span></span></p></td>
<td><p><span data-ttu-id="4715b-124">キューブの名前。</span><span class="sxs-lookup"><span data-stu-id="4715b-124">The name of the cube.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4715b-125">CubeType</span><span class="sxs-lookup"><span data-stu-id="4715b-125">CubeType</span></span></p></td>
<td><p><span data-ttu-id="4715b-126">キューブの種類。</span><span class="sxs-lookup"><span data-stu-id="4715b-126">The type of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4715b-127">DataUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="4715b-127">DataUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="4715b-128">最後にデータを更新したユーザーの ID。</span><span class="sxs-lookup"><span data-stu-id="4715b-128">User ID of the person doing the last data update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4715b-129">Description</span><span class="sxs-lookup"><span data-stu-id="4715b-129">Description</span></span></p></td>
<td><p><span data-ttu-id="4715b-130">キューブの説明。</span><span class="sxs-lookup"><span data-stu-id="4715b-130">A meaningful description of the cube.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4715b-131">LastSchemaUpdate</span><span class="sxs-lookup"><span data-stu-id="4715b-131">LastSchemaUpdate</span></span></p></td>
<td><p><span data-ttu-id="4715b-132">最後にスキーマを更新した日時。</span><span class="sxs-lookup"><span data-stu-id="4715b-132">Date and time of last schema update.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4715b-133">スキーマ名</span><span class="sxs-lookup"><span data-stu-id="4715b-133">SchemaName</span></span></p></td>
<td><p><span data-ttu-id="4715b-134">このキューブが属しているスキーマの名前。</span><span class="sxs-lookup"><span data-stu-id="4715b-134">The name of the schema to which this cube belongs.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4715b-135">SchemaUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="4715b-135">SchemaUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="4715b-136">最後にスキーマを更新したユーザーの ID。</span><span class="sxs-lookup"><span data-stu-id="4715b-136">User ID of the person doing the last schema update.</span></span></p></td>
</tr>
</tbody>
</table>

