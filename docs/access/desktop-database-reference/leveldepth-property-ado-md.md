---
title: LevelDepth プロパティ (ADO MD)
TOCTitle: LevelDepth Property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 74be66479fbd911979401b66e5af2e2f62ade646
ms.sourcegitcommit: c557bbcccf37a6011f89aae1ddd399dfe549d087
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/31/2018
ms.locfileid: "25882470"
---
# <a name="leveldepth-property-ado-md"></a><span data-ttu-id="fd2f6-102">LevelDepth プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="fd2f6-102">LevelDepth Property (ADO MD)</span></span>


<span data-ttu-id="fd2f6-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="fd2f6-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="fd2f6-104">階層のルートとメンバーとの間にあるレベルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="fd2f6-104">Indicates the number of levels between the root of the hierarchy and a member.</span></span>

## <a name="return-values"></a><span data-ttu-id="fd2f6-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="fd2f6-105">Return values</span></span>

<span data-ttu-id="fd2f6-106">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="fd2f6-106">Returns a **Long** integer, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="fd2f6-107">解説</span><span class="sxs-lookup"><span data-stu-id="fd2f6-107">Remarks</span></span>

<span data-ttu-id="fd2f6-p101">**LevelDepth** プロパティを使用して、階層のルート レベルから [Member](member-object-ado-md.md) オブジェクトまでの距離を調べます。ルート レベルにあるメンバーの **LevelDepth** は 0 です。このプロパティは、 [Level](depth-property-ado-md.md) オブジェクトの [Depth](level-object-ado-md.md) プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="fd2f6-p101">Use the **LevelDepth** property to determine the distance of the [Member](member-object-ado-md.md) object from the root level of the hierarchy. The **LevelDepth** of a member at the root level is 0. This corresponds to the [Depth](depth-property-ado-md.md) property of a [Level](level-object-ado-md.md) object.</span></span>

