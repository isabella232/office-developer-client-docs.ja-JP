---
title: FilterAxis プロパティ (ADO MD)
TOCTitle: FilterAxis Property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 32ddf737ae0d6aa9a7b2daf8adc2a07707c91c0c
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603057"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="e5e88-102">FilterAxis プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="e5e88-102">FilterAxis Property (ADO MD)</span></span>


<span data-ttu-id="e5e88-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="e5e88-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="e5e88-104">現在のセルセットのフィルター情報を示します。</span><span class="sxs-lookup"><span data-stu-id="e5e88-104">Indicates filter information about the current cellset.</span></span>

<span data-ttu-id="e5e88-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="e5e88-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="e5e88-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="e5e88-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="e5e88-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="e5e88-107">Return values</span></span>
>>>>>>> <span data-ttu-id="e5e88-108">master</span><span class="sxs-lookup"><span data-stu-id="e5e88-108">master</span></span>

<span data-ttu-id="e5e88-109">[Axis](axis-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="e5e88-109">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="e5e88-110">解説</span><span class="sxs-lookup"><span data-stu-id="e5e88-110">Remarks</span></span>

<span data-ttu-id="e5e88-p101">**FilterAxis** プロパティを使用すると、データをスライスするために使用した次元の情報を取得できます。 [Axis](dimensioncount-property-ado-md.md) オブジェクトの **DimensionCount** プロパティは、スライスする次元の数を返します。この軸には通常、行が 1 つだけ含まれます。</span><span class="sxs-lookup"><span data-stu-id="e5e88-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="e5e88-114">**FilterAxis** によって取得される [Axis](filteraxis-property-ado-md.md) オブジェクトは、 [Cellset](axes-collection-ado-md.md) オブジェクトの [Axes](cellset-object-ado-md.md) コレクションには含まれません。</span><span class="sxs-lookup"><span data-stu-id="e5e88-114">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

