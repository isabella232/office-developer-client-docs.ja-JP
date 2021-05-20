---
title: '[X] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: ローカル座標の接続点の x 座標を表します。
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436784"
---
# <a name="x-cell-connection-points-section"></a><span data-ttu-id="6039d-103">[X] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="6039d-103">X Cell (Connection Points Section)</span></span>

<span data-ttu-id="6039d-104">ローカル座標の  *接続点*  の x 座標を表します。</span><span class="sxs-lookup"><span data-stu-id="6039d-104">Represents the  *x*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6039d-105">注釈</span><span class="sxs-lookup"><span data-stu-id="6039d-105">Remarks</span></span>

<span data-ttu-id="6039d-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="6039d-106">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6039d-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="6039d-107">Cell name:</span></span>  <br/> | <span data-ttu-id="6039d-108">Connections.X  *i*            *は、i*  = <1>、2、3..です。</span><span class="sxs-lookup"><span data-stu-id="6039d-108">Connections.X  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6039d-109">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="6039d-109">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6039d-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6039d-110">Section index:</span></span>  <br/> |<span data-ttu-id="6039d-111">**visSectionConnectionPts**</span><span class="sxs-lookup"><span data-stu-id="6039d-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="6039d-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6039d-112">Row index:</span></span>  <br/> |<span data-ttu-id="6039d-113">**visRowConnectionPts**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6039d-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6039d-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6039d-114">Cell index:</span></span>  <br/> |<span data-ttu-id="6039d-115">**visX**</span><span class="sxs-lookup"><span data-stu-id="6039d-115">**visX**</span></span> <br/> |
   

