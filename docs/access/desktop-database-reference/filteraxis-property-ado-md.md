---
title: FilterAxis プロパティ (ADO MD)
TOCTitle: FilterAxis property (ADO MD)
ms:assetid: 36720d77-4b16-1d17-6d80-d35265f4a8ad
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249124(v=office.15)
ms:contentKeyID: 48544172
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 214de72e71a51c6b6b65bc2636a28e5650035c0a
ms.sourcegitcommit: d7248f803002b31cf7fc561b03530199a9b0a8fd
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/02/2018
ms.locfileid: "25926907"
---
# <a name="filteraxis-property-ado-md"></a><span data-ttu-id="f526d-102">FilterAxis プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="f526d-102">FilterAxis property (ADO MD)</span></span>


<span data-ttu-id="f526d-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="f526d-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="f526d-104">現在のセルセットのフィルター情報を示します。</span><span class="sxs-lookup"><span data-stu-id="f526d-104">Indicates filter information about the current cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="f526d-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="f526d-105">Return values</span></span>

<span data-ttu-id="f526d-106">[Axis](axis-object-ado-md.md) オブジェクトを取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="f526d-106">Returns an [Axis](axis-object-ado-md.md) object, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="f526d-107">解説</span><span class="sxs-lookup"><span data-stu-id="f526d-107">Remarks</span></span>

<span data-ttu-id="f526d-p101">**FilterAxis** プロパティを使用すると、データをスライスするために使用した次元の情報を取得できます。 [Axis](dimensioncount-property-ado-md.md) オブジェクトの **DimensionCount** プロパティは、スライスする次元の数を返します。この軸には通常、行が 1 つだけ含まれます。</span><span class="sxs-lookup"><span data-stu-id="f526d-p101">Use the **FilterAxis** property to return information about the dimensions that were used to slice the data. The [DimensionCount](dimensioncount-property-ado-md.md) property of the **Axis** returns the number of slicer dimensions. This axis usually has just one row.</span></span>

<span data-ttu-id="f526d-111">**FilterAxis** によって取得される [Axis](filteraxis-property-ado-md.md) オブジェクトは、 [Cellset](axes-collection-ado-md.md) オブジェクトの [Axes](cellset-object-ado-md.md) コレクションには含まれません。</span><span class="sxs-lookup"><span data-stu-id="f526d-111">The **Axis** returned by [FilterAxis](filteraxis-property-ado-md.md) is not contained in the [Axes](axes-collection-ado-md.md) collection for a [Cellset](cellset-object-ado-md.md) object.</span></span>

