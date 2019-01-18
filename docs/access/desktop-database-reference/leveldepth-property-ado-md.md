---
title: LevelDepth プロパティ (ADO MD)
TOCTitle: LevelDepth property (ADO MD)
ms:assetid: ba680f1e-2731-ad6b-4cee-cd3d8d114788
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249894(v=office.15)
ms:contentKeyID: 48547366
ms.date: 09/18/2015
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 664a21f8b642c8db27580993089268e5d7b6f4ae
ms.sourcegitcommit: d6695c94415fa47952ee7961a69660abc0904434
ms.translationtype: Auto
ms.contentlocale: ja-JP
ms.lasthandoff: 01/17/2019
ms.locfileid: "28708565"
---
# <a name="leveldepth-property-ado-md"></a><span data-ttu-id="dc052-102">LevelDepth プロパティ (ADO MD)</span><span class="sxs-lookup"><span data-stu-id="dc052-102">LevelDepth property (ADO MD)</span></span>


<span data-ttu-id="dc052-103">**適用されます**Access 2013、Office 2013。</span><span class="sxs-lookup"><span data-stu-id="dc052-103">**Applies to**: Access 2013, Office 2013</span></span>

<span data-ttu-id="dc052-104">階層のルートとメンバーとの間にあるレベルの数を示します。</span><span class="sxs-lookup"><span data-stu-id="dc052-104">Indicates the number of levels between the root of the hierarchy and a member.</span></span>

## <a name="return-values"></a><span data-ttu-id="dc052-105">戻り値</span><span class="sxs-lookup"><span data-stu-id="dc052-105">Return values</span></span>

<span data-ttu-id="dc052-106">長整数型 ( **Long** ) の値を取得します。値の取得のみが可能です。</span><span class="sxs-lookup"><span data-stu-id="dc052-106">Returns a **Long** integer, and is read-only.</span></span>

## <a name="remarks"></a><span data-ttu-id="dc052-107">解説</span><span class="sxs-lookup"><span data-stu-id="dc052-107">Remarks</span></span>

<span data-ttu-id="dc052-p101">**LevelDepth** プロパティを使用して、階層のルート レベルから [Member](member-object-ado-md.md) オブジェクトまでの距離を調べます。ルート レベルにあるメンバーの **LevelDepth** は 0 です。このプロパティは、 [Level](depth-property-ado-md.md) オブジェクトの [Depth](level-object-ado-md.md) プロパティに対応します。</span><span class="sxs-lookup"><span data-stu-id="dc052-p101">Use the **LevelDepth** property to determine the distance of the [Member](member-object-ado-md.md) object from the root level of the hierarchy. The **LevelDepth** of a member at the root level is 0. This corresponds to the [Depth](depth-property-ado-md.md) property of a [Level](level-object-ado-md.md) object.</span></span>

