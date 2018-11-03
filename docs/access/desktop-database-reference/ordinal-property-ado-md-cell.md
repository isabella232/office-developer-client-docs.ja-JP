---
title: Ordinal プロパティ (ADO MD Cell)
TOCTitle: Ordinal property (ADO MD Cell)
ms:assetid: be705823-6c5e-0c8f-f780-87df19423a72
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249924(v=office.15)
ms:contentKeyID: 48547462
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 4fbbe461390a5f8a068f839bcf41fab5e1ad66ff
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25946756"
---
# <a name="ordinal-property-ado-md-cell"></a><span data-ttu-id="34f68-102">Ordinal プロパティ (ADO MD Cell)</span><span class="sxs-lookup"><span data-stu-id="34f68-102">Ordinal property (ADO MD Cell)</span></span>


<span data-ttu-id="34f68-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="34f68-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="34f68-104">セルセット内の位置によってセルを一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="34f68-104">Uniquely identifies a cell by its position within a cellset.</span></span>

## <a name="return-values"></a><span data-ttu-id="34f68-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="34f68-105">Return values</span></span>

<span data-ttu-id="34f68-106">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="34f68-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="34f68-107">解説</span><span class="sxs-lookup"><span data-stu-id="34f68-107">Remarks</span></span>

<span data-ttu-id="34f68-p101">セルの序数値はセルセット内のセルを一意に識別します。概念的は、セルセット内のセルはセルセットが *p* 番号が付けられます。ここで、*p* は[軸](axes-collection-ado-md.md)の数です。セルは行優先でアドレス指定されます。</span><span class="sxs-lookup"><span data-stu-id="34f68-p101">The cell's ordinal value uniquely identifies the cell within a cellset. Conceptually, cells are numbered in a cellset as if the cellset were a *p*-dimensional array, where *p* is the number of [axes](axes-collection-ado-md.md). Cells are numbered starting from zero in row-major order.</span></span>

<span data-ttu-id="34f68-111">セルの序数値は [Cellset](item-property-ado-md-cellset.md) オブジェクトの [Item](cellset-object-ado-md.md) プロパティと共に使用して、 [Cell](cell-object-ado-md.md) を迅速に取得できます。</span><span class="sxs-lookup"><span data-stu-id="34f68-111">The cell's ordinal value can be used with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object to quickly retrieve the [Cell](cell-object-ado-md.md).</span></span>

