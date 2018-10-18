---
title: Ordinal プロパティ (ADO MD Position)
TOCTitle: Ordinal Property (ADO MD Position)
ms:assetid: fb132ab5-d2b5-317d-e885-5e37ddaf90fb
ms:mtpsurl: https://msdn.microsoft.com/library/JJ250284(v=office.15)
ms:contentKeyID: 48548861
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: d3d629002fb11547ffbb9f3823b161e189ee4d45
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25603253"
---
# <a name="ordinal-property-ado-md-position"></a><span data-ttu-id="1f0c1-102">Ordinal プロパティ (ADO MD Position)</span><span class="sxs-lookup"><span data-stu-id="1f0c1-102">Ordinal Property (ADO MD Position)</span></span>


<span data-ttu-id="1f0c1-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="1f0c1-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="1f0c1-104">軸に沿った位置を一意に識別します。</span><span class="sxs-lookup"><span data-stu-id="1f0c1-104">Uniquely identifies a position along an axis.</span></span>

<span data-ttu-id="1f0c1-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="1f0c1-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="1f0c1-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="1f0c1-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="1f0c1-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="1f0c1-107">Return values</span></span>
>>>>>>> <span data-ttu-id="1f0c1-108">master</span><span class="sxs-lookup"><span data-stu-id="1f0c1-108">master</span></span>

<span data-ttu-id="1f0c1-109">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="1f0c1-109">Returns a **Long** integer and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="1f0c1-110">解説</span><span class="sxs-lookup"><span data-stu-id="1f0c1-110">Remarks</span></span>

<span data-ttu-id="1f0c1-111">**Position** オブジェクトの [Ordinal](position-object-ado-md.md) プロパティは、 **Positions** コレクション内の [Position](positions-collection-ado-md.md) のインデックスに対応します。</span><span class="sxs-lookup"><span data-stu-id="1f0c1-111">The **Ordinal** of a [Position](position-object-ado-md.md) object corresponds to the index of the **Position** within the [Positions](positions-collection-ado-md.md) collection.</span></span>

<span data-ttu-id="1f0c1-112">**Cellset** オブジェクトの **Item** プロパティでそれぞれの軸に沿って [Position](item-property-ado-md-cellset.md) オブジェクトの [Ordinal](cellset-object-ado-md.md) プロパティを使用することで、セルをすばやく取得できます。</span><span class="sxs-lookup"><span data-stu-id="1f0c1-112">A cell can quickly be retrieved using the **Ordinal** of the **Position** along each axis with the [Item](item-property-ado-md-cellset.md) property of the [Cellset](cellset-object-ado-md.md) object.</span></span>

