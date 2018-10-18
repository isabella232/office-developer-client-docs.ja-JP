---
title: LevelDepth プロパティ (ADO MD)
TOCTitle: LevelDepth Property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 80712421cc146e482f848a997fe5f2d95cd951b1
ms.sourcegitcommit: a49b77f4c8cec69f90656a86f0872cf34c35968e
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/17/2018
ms.locfileid: "25604275"
---
# <a name="leveldepth-property-ado-md"></a><span data-ttu-id="06d7c-102">LevelDepth プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="06d7c-102">LevelDepth Property (ADO MD)</span></span>


<span data-ttu-id="06d7c-103">**適用されます**Access 2013 |。Office 2013</span><span class="sxs-lookup"><span data-stu-id="06d7c-103">**Applies to**: Access 2013 | Office 2013</span></span>

<span data-ttu-id="06d7c-104">階層のルートとメンバーとの間にあるレベルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="06d7c-104">Indicates the number of levels between the root of the hierarchy and a member.</span></span>

<span data-ttu-id="06d7c-105"><<<<<<< ヘッド</span><span class="sxs-lookup"><span data-stu-id="06d7c-105"><<<<<<< HEAD</span></span>
## <a name="return-values"></a><span data-ttu-id="06d7c-106">戻り値</span><span class="sxs-lookup"><span data-stu-id="06d7c-106">Return Values</span></span>
=======
## <a name="return-values"></a><span data-ttu-id="06d7c-107">戻り値</span><span class="sxs-lookup"><span data-stu-id="06d7c-107">Return values</span></span>
>>>>>>> <span data-ttu-id="06d7c-108">master</span><span class="sxs-lookup"><span data-stu-id="06d7c-108">master</span></span>

<span data-ttu-id="06d7c-109">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="06d7c-109">Returns a **Long** integer, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="06d7c-110">解説</span><span class="sxs-lookup"><span data-stu-id="06d7c-110">Remarks</span></span>

<span data-ttu-id="06d7c-p101">**LevelDepth** プロパティを使用して、階層のルート レベルから [Member](member-object-ado-md.md) オブジェクトまでの距離を調べます。ルート レベルにあるメンバーの **LevelDepth** は 0 です。このプロパティは、 [Level](depth-property-ado-md.md) オブジェクトの [Depth](level-object-ado-md.md) プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="06d7c-p101">Use the **LevelDepth** property to determine the distance of the [Member](member-object-ado-md.md) object from the root level of the hierarchy. The **LevelDepth** of a member at the root level is 0. This corresponds to the [Depth](depth-property-ado-md.md) property of a [Level](level-object-ado-md.md) object.</span></span>

