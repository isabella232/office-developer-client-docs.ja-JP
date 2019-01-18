---
title: FilterAxis プロパティ (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 3b1f9c2bcc4ed4f3314a697d4a0eae8415bc4f62
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28713269"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="4d1bf-102">FilterAxis プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="4d1bf-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="4d1bf-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="4d1bf-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="4d1bf-104">現在のセルセットのフィルター情報を示します。</span><span class="sxs-lookup"><span data-stu-id="4d1bf-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="4d1bf-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="4d1bf-105">Return values</span></span>

<span data-ttu-id="4d1bf-106">[Axis](axis-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="4d1bf-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d1bf-107">解説</span><span class="sxs-lookup"><span data-stu-id="4d1bf-107">Remarks</span></span>

<span data-ttu-id="4d1bf-p101">**FilterAxis** プロパティを使用すると、データをスライスするために使用した次元の情報を取得できます。 [Axis](dimensioncount-property-ado-md.md) オブジェクトの **DimensionCount** プロパティは、スライスする次元の数を返します。この軸には通常、行が 1 つだけ含まれます。</span><span class="sxs-lookup"><span data-stu-id="4d1bf-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="4d1bf-111">**FilterAxis** によって取得される [Axis](filteraxis-property-ado-md.md) オブジェクトは、 [Cellset](axes-collection-ado-md.md) オブジェクトの [Axes](cellset-object-ado-md.md) コレクションには含まれません。</span><span class="sxs-lookup"><span data-stu-id="4d1bf-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

