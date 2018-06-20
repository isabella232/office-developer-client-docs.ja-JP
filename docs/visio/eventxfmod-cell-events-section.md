---
title: '[EventXFMod] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: 図形の位置や、ページの向きは、するときに評価されるイベント セルは、(XF) を変換します。
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805350"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="67f77-103">[EventXFMod] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="67f77-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="67f77-104">ページ上で、図形の位置または向きの変更 ("XF") が行われたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="67f77-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="67f77-105">備考</span><span class="sxs-lookup"><span data-stu-id="67f77-105">Remarks</span></span>

<span data-ttu-id="67f77-106">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="67f77-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="67f77-107">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [eventxfmod] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="67f77-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67f77-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="67f77-108">Cell name:</span></span>  <br/> | <span data-ttu-id="67f77-109">[Eventxfmod]</span><span class="sxs-lookup"><span data-stu-id="67f77-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="67f77-110">プログラムから、インデックスによって [eventxfmod] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="67f77-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="67f77-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="67f77-111">Section index:</span></span>  <br/> |<span data-ttu-id="67f77-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="67f77-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="67f77-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="67f77-113">Row index:</span></span>  <br/> |<span data-ttu-id="67f77-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="67f77-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="67f77-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="67f77-115">Cell index:</span></span>  <br/> |<span data-ttu-id="67f77-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="67f77-116">**visEvtCellXFMod**</span></span> <br/> |
   

