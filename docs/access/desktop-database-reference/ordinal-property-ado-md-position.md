---
title: Ordinal プロパティ (ADO MD Position)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: abf355cc4d066604035fddbbe8f8a428d8c7a6b0
ms.sourcegitcommit: 558d09fad81f8d80b5ad0edd21934fc09c098f2c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 11/03/2018
ms.locfileid: "25944782"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="d118e-102">Ordinal プロパティ (ADO MD Position)</span><span class="sxs-lookup"><span data-stu-id="d118e-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="d118e-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="d118e-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="d118e-104">軸に沿った位置を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="d118e-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="d118e-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="d118e-105">Return values</span></span>

<span data-ttu-id="d118e-106">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="d118e-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="d118e-107">解説</span><span class="sxs-lookup"><span data-stu-id="d118e-107">Remarks</span></span>

<span data-ttu-id="d118e-108">**Position** オブジェクトの [Ordinal](position-object-ado-md.md) プロパティは、 **Positions** コレクション内の [Position](positions-collection-ado-md.md) のインデックスに対応します。</span><span class="sxs-lookup"><span data-stu-id="d118e-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="d118e-109">**Cellset** オブジェクトの **Item** プロパティでそれぞれの軸に沿って [Position](item-property-ado-md-cellset.md) オブジェクトの [Ordinal](cellset-object-ado-md.md) プロパティを使用することで、セルをすばやく取得できます。</span><span class="sxs-lookup"><span data-stu-id="d118e-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

