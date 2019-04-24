---
title: '[EventDrop] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: 図面ページに図形をインスタンスとしてドロップしたとき、または図形を複製したり貼り付けたときに評価されるイベント セルです。
ms.openlocfilehash: f1433394dbd58c7c4422c6bca1e79a4f2c8e0c4e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351010"
---
# <a name="eventdrop-cell-events-section"></a><span data-ttu-id="c8b21-103">[EventDrop] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="c8b21-103">EventDrop Cell (Events Section)</span></span>

<span data-ttu-id="c8b21-104">図面ページに図形をインスタンスとしてドロップしたとき、または図形を複製したり貼り付けたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="c8b21-104">An event cell that is evaluated when a shape is dropped on the drawing page, either as an instance or when the shape is duplicated or pasted.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c8b21-105">解説</span><span class="sxs-lookup"><span data-stu-id="c8b21-105">Remarks</span></span>

<span data-ttu-id="c8b21-106">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="c8b21-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="c8b21-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventDrop] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="c8b21-107">To get a reference to the EventDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8b21-108">セル名 :</span><span class="sxs-lookup"><span data-stu-id="c8b21-108">Cell name:</span></span>  <br/> | <span data-ttu-id="c8b21-109">[eventdrop]</span><span class="sxs-lookup"><span data-stu-id="c8b21-109">EventDrop</span></span>  <br/> |
   
<span data-ttu-id="c8b21-110">プログラムから、インデックスによって [EventDrop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="c8b21-110">To get a reference to the EventDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c8b21-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8b21-111">Section index:</span></span>  <br/> |<span data-ttu-id="c8b21-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c8b21-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c8b21-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8b21-113">Row index:</span></span>  <br/> |<span data-ttu-id="c8b21-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="c8b21-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="c8b21-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c8b21-115">Cell index:</span></span>  <br/> |<span data-ttu-id="c8b21-116">**visEvtCellDrop**</span><span class="sxs-lookup"><span data-stu-id="c8b21-116">**visEvtCellDrop**</span></span> <br/> |
   

