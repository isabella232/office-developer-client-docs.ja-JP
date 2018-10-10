---
title: FilterAxis プロパティ (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 912dfec595f718c2144e69b4fbd3af592f8b6d5b
ms.sourcegitcommit: 19aca09c5812cfb98b68b5d4604dcaa814479df7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/09/2018
ms.locfileid: "25477424"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="dec97-102">FilterAxis プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="dec97-102">FilterAxis Property (ADO MD)</span></span>


<span data-ttu-id="dec97-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="dec97-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="dec97-104">現在のセルセットのフィルター情報を示します。</span><span class="sxs-lookup"><span data-stu-id="dec97-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="dec97-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="dec97-105">Return Values</span></span>

<span data-ttu-id="dec97-106">[Axis](axis-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="dec97-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="dec97-107">解説</span><span class="sxs-lookup"><span data-stu-id="dec97-107">Remarks</span></span>

<span data-ttu-id="dec97-p101">**FilterAxis** プロパティを使用すると、データをスライスするために使用した次元の情報を取得できます。 [Axis](dimensioncount-property-ado-md.md) オブジェクトの **DimensionCount** プロパティは、スライスする次元の数を返します。この軸には通常、行が 1 つだけ含まれます。</span><span class="sxs-lookup"><span data-stu-id="dec97-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="dec97-111">**FilterAxis** によって取得される [Axis](filteraxis-property-ado-md.md) オブジェクトは、 [Cellset](axes-collection-ado-md.md) オブジェクトの [Axes](cellset-object-ado-md.md) コレクションには含まれません。</span><span class="sxs-lookup"><span data-stu-id="dec97-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

