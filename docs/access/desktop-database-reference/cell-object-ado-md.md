---
title: Cell オブジェクト (ADO MD)
TOCTitle: Cell object (ADO MD)
ms:assetid: b9d00b71-1f40-5bd1-4b89-fbdb59c552ba
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249892(v=office.15)
ms:contentKeyID: 48547356
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 2e119600567c8d3c6cd23348d9b9560011e27a87
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25924611"
---
# <a name="cell-object-ado-md"></a><span data-ttu-id="6f2c0-102">Cell オブジェクト (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="6f2c0-102">Cell object (ADO MD)</span></span>


<span data-ttu-id="6f2c0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="6f2c0-104">セルセットに含まれる、座標軸の交点のデータを表します。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-104">Represents the data at the intersection of axis coordinates contained in a cellset.</span></span>

## <a name="remarks"></a><span data-ttu-id="6f2c0-105">解説</span><span class="sxs-lookup"><span data-stu-id="6f2c0-105">Remarks</span></span>

<span data-ttu-id="6f2c0-106">**Cell** オブジェクトは、 [Cellset](item-property-ado-md-cellset.md) オブジェクトの [Item](cellset-object-ado-md.md) プロパティによって返されます。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-106">A **Cell** object is returned by the [Item](item-property-ado-md-cellset.md) property of a [Cellset](cellset-object-ado-md.md) object.</span></span>

<span data-ttu-id="6f2c0-107">**Cell** オブジェクトのコレクションおよびプロパティを使用すると、次の操作を実行できます。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-107">With the collections and properties of a **Cell** object, you can do the following:</span></span>

  - <span data-ttu-id="6f2c0-108">**Value** プロパティを使用して、 [Cell](value-property-ado-md.md) のデータを返します。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-108">Return the data in the **Cell** with the [Value](value-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="6f2c0-109">**FormattedValue** プロパティを使用して、 [Value](formattedvalue-property-ado-md.md) プロパティの書式設定された表示文字列を返します。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-109">Return the string representing the formatted display of the **Value** property with the [FormattedValue](formattedvalue-property-ado-md.md) property.</span></span>

  - <span data-ttu-id="6f2c0-110">**Ordinal** プロパティを使用して、 **Cellset** 内の [Cell](ordinal-property-ado-md-cell.md) の序数値を返します。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-110">Return the ordinal value of the **Cell** within the **Cellset** with the [Ordinal](ordinal-property-ado-md-cell.md) property.</span></span>

  - <span data-ttu-id="6f2c0-111">**Positions** コレクションを使用して、 [CubeDef](cubedef-object-ado-md.md) 内の [Cell](positions-collection-ado-md.md) の位置を特定します。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-111">Determine the position of the **Cell** within the [CubeDef](cubedef-object-ado-md.md) with the [Positions](positions-collection-ado-md.md) collection.</span></span>

  - <span data-ttu-id="6f2c0-112">標準の ADO **Properties** コレクションを使用して、 [Cell](properties-collection-ado.md) に関するその他の情報を取得します。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-112">Retrieve other information about the **Cell** with the standard ADO [Properties](properties-collection-ado.md) collection.</span></span>

<span data-ttu-id="6f2c0-p101">**Properties** コレクションには、プロバイダー固有のプロパティが含まれます。次の表に、使用できるプロパティを示します。実際に使用できるプロパティの一覧は、プロバイダーの実装によって異なります。使用できるプロパティの完全な一覧については、各自のプロバイダーのドキュメントを参照してください。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-p101">The **Properties** collection contains provider-supplied properties. The following table lists properties that might be available. The actual property list may differ depending upon the implementation of the provider. See the documentation for your provider for a more complete list of available properties.</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p><span data-ttu-id="6f2c0-117">名前</span><span class="sxs-lookup"><span data-stu-id="6f2c0-117">Name</span></span></p></th>
<th><p><span data-ttu-id="6f2c0-118">説明</span><span class="sxs-lookup"><span data-stu-id="6f2c0-118">Description</span></span></p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6f2c0-119">BackColor</span><span class="sxs-lookup"><span data-stu-id="6f2c0-119">BackColor</span></span></p></td>
<td><p><span data-ttu-id="6f2c0-120">セルを表示するときに使用する背景色。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-120">Background color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f2c0-121">FontFlags</span><span class="sxs-lookup"><span data-stu-id="6f2c0-121">FontFlags</span></span></p></td>
<td><p><span data-ttu-id="6f2c0-122">フォントの効果を指定するビットマスク。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-122">Bitmask detailing effects on the font.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f2c0-123">FontName</span><span class="sxs-lookup"><span data-stu-id="6f2c0-123">FontName</span></span></p></td>
<td><p><span data-ttu-id="6f2c0-124">セル値を表示するために使用するフォント。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-124">Font used to display the cell value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f2c0-125">フォント サイズ</span><span class="sxs-lookup"><span data-stu-id="6f2c0-125">FontSize</span></span></p></td>
<td><p><span data-ttu-id="6f2c0-126">セル値を表示するために使用するフォントのサイズ。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-126">Font size used to display the cell value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6f2c0-127">ForeColor</span><span class="sxs-lookup"><span data-stu-id="6f2c0-127">ForeColor</span></span></p></td>
<td><p><span data-ttu-id="6f2c0-128">セルを表示するときに使用する前景色。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-128">Foreground color used when displaying the cell.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6f2c0-129">FormatString</span><span class="sxs-lookup"><span data-stu-id="6f2c0-129">FormatString</span></span></p></td>
<td><p><span data-ttu-id="6f2c0-130">書式設定された文字列の値。</span><span class="sxs-lookup"><span data-stu-id="6f2c0-130">Value in a formatted string.</span></span></p></td>
</tr>
</tbody>
</table>

