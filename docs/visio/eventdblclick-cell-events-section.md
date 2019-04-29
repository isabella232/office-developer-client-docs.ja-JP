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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438219"
---
# <a name="eventdblclick-cell-events-section"></a><span data-ttu-id="42102-103">[EventDblClick] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="42102-103">EventDblClick Cell (Events Section)</span></span>

<span data-ttu-id="42102-104">図形をダブルクリックしたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="42102-104">An event cell that is evaluated when a shape is double-clicked.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42102-105">注釈</span><span class="sxs-lookup"><span data-stu-id="42102-105">Remarks</span></span>

<span data-ttu-id="42102-106">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="42102-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="42102-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventDblClick] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="42102-107">To get a reference to the EventDblClick cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42102-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="42102-108">Cell name:</span></span>  <br/> | <span data-ttu-id="42102-109">eventdblclick]</span><span class="sxs-lookup"><span data-stu-id="42102-109">EventDblClick</span></span>  <br/> |
   
<span data-ttu-id="42102-110">プログラムから、インデックスによって [EventDblClick] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="42102-110">To get a reference to the EventDblClick cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="42102-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="42102-111">Section index:</span></span>  <br/> |<span data-ttu-id="42102-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="42102-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="42102-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="42102-113">Row index:</span></span>  <br/> |<span data-ttu-id="42102-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="42102-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="42102-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="42102-115">Cell index:</span></span>  <br/> |<span data-ttu-id="42102-116">**visEvtCellDblClick**</span><span class="sxs-lookup"><span data-stu-id="42102-116">**visEvtCellDblClick**</span></span> <br/> |
   

