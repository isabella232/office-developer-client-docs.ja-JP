---
title: '[Y] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: 接続ポイントの y 座標をローカル座標で表します。
ms.openlocfilehash: b408dc3c07e7bd28c0530b09f649453b4f08c770
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410848"
---
# <a name="y-cell-connection-points-section"></a><span data-ttu-id="5eb69-103">[Y] セル ([Connection Points] セクション)</span><span class="sxs-lookup"><span data-stu-id="5eb69-103">Y Cell (Connection Points Section)</span></span>

<span data-ttu-id="5eb69-104">接続ポイントの*y*座標をローカル座標で表します。</span><span class="sxs-lookup"><span data-stu-id="5eb69-104">Represents the  *y*  -coordinate for a connection point in local coordinates.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5eb69-105">注釈</span><span class="sxs-lookup"><span data-stu-id="5eb69-105">Remarks</span></span>

<span data-ttu-id="5eb69-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5eb69-106">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5eb69-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="5eb69-107">Cell name:</span></span>  <br/> | <span data-ttu-id="5eb69-108">接続 Y *i* = <1> \*\* 、2、3...</span><span class="sxs-lookup"><span data-stu-id="5eb69-108">Connections.Y  *i*            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="5eb69-109">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5eb69-109">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5eb69-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5eb69-110">Section index:</span></span>  <br/> |<span data-ttu-id="5eb69-111">**持つ vissectionconnectionpts**</span><span class="sxs-lookup"><span data-stu-id="5eb69-111">**visSectionConnectionPts**</span></span> <br/> |
| <span data-ttu-id="5eb69-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5eb69-112">Row index:</span></span>  <br/> |<span data-ttu-id="5eb69-113">**visRowConnectionPts** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="5eb69-113">**visRowConnectionPts** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="5eb69-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5eb69-114">Cell index:</span></span>  <br/> |<span data-ttu-id="5eb69-115">**visY**</span><span class="sxs-lookup"><span data-stu-id="5eb69-115">**visY**</span></span> <br/> |
   

