---
title: Ordinal プロパティ (ADO MD Position)
TOCTitle: Ordinal property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 2e29b5c86e8f37d84116aa92432e93eb8943e29e
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28711744"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="bc9a0-102">Ordinal プロパティ (ADO MD Position)</span><span class="sxs-lookup"><span data-stu-id="bc9a0-102">Ordinal property (ADO MD Position)</span></span>


<span data-ttu-id="bc9a0-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="bc9a0-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="bc9a0-104">軸に沿った位置を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="bc9a0-104">Uniquely identifies a position along an axis.</span></span>

## <a name="return-values"></a><span data-ttu-id="bc9a0-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="bc9a0-105">Return values</span></span>

<span data-ttu-id="bc9a0-106">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="bc9a0-106">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="bc9a0-107">解説</span><span class="sxs-lookup"><span data-stu-id="bc9a0-107">Remarks</span></span>

<span data-ttu-id="bc9a0-108">**Position** オブジェクトの [Ordinal](position-object-ado-md.md) プロパティは、 **Positions** コレクション内の [Position](positions-collection-ado-md.md) のインデックスに対応します。</span><span class="sxs-lookup"><span data-stu-id="bc9a0-108">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="bc9a0-109">**Cellset** オブジェクトの **Item** プロパティでそれぞれの軸に沿って [Position](item-property-ado-md-cellset.md) オブジェクトの [Ordinal](cellset-object-ado-md.md) プロパティを使用することで、セルをすばやく取得できます。</span><span class="sxs-lookup"><span data-stu-id="bc9a0-109">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

