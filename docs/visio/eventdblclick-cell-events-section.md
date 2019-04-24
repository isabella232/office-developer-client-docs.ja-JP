---
title: '[EventDblClick] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: 図形をダブルクリックしたときに評価されるイベント セルです。
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337171"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="b2d04-103">[EventDblClick] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="b2d04-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="b2d04-104">図形をダブルクリックしたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="b2d04-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b2d04-105">解説</span><span class="sxs-lookup"><span data-stu-id="b2d04-105">Remarks</span></span>

<span data-ttu-id="b2d04-106">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="b2d04-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="b2d04-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventDblClick] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b2d04-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2d04-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="b2d04-108">Cell name:</span></span>  <br/> | <span data-ttu-id="b2d04-109">eventdblclick]</span><span class="sxs-lookup"><span data-stu-id="b2d04-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="b2d04-110">プログラムから、インデックスによって [EventDblClick] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b2d04-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b2d04-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b2d04-111">Section index:</span></span>  <br/> |<span data-ttu-id="b2d04-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b2d04-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b2d04-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b2d04-113">Row index:</span></span>  <br/> |<span data-ttu-id="b2d04-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="b2d04-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="b2d04-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b2d04-115">Cell index:</span></span>  <br/> |<span data-ttu-id="b2d04-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="b2d04-116">**visEvtCellDblClick**</span></span> <br/> |
   

