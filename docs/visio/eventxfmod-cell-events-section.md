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
description: ページ上の図形の位置または向きが変換 (XF) されたときに評価されるイベントセルです。
ms.openlocfilehash: c4ed4ddd9b255a9a52fc81349b514dbd25772c98
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418534"
---
# <a name="eventxfmod-cell-events-section"></a><span data-ttu-id="dae1c-103">[EventXFMod] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="dae1c-103">EventXFMod Cell (Events Section)</span></span>

<span data-ttu-id="dae1c-104">ページ上で、図形の位置または向きの変更 ("XF") が行われたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="dae1c-104">An event cell that is evaluated when a shape's position or orientation on the page is transformed ("XF").</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dae1c-105">注釈</span><span class="sxs-lookup"><span data-stu-id="dae1c-105">Remarks</span></span>

<span data-ttu-id="dae1c-106">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="dae1c-106">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="dae1c-107">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventXFMod] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="dae1c-107">To get a reference to the EventXFMod cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dae1c-108">セル名:</span><span class="sxs-lookup"><span data-stu-id="dae1c-108">Cell name:</span></span>  <br/> | <span data-ttu-id="dae1c-109">[eventxfmod]</span><span class="sxs-lookup"><span data-stu-id="dae1c-109">EventXFMod</span></span>  <br/> |
   
<span data-ttu-id="dae1c-110">プログラムから、インデックスによって [EventXFMod] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dae1c-110">To get a reference to the EventXFMod cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dae1c-111">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dae1c-111">Section index:</span></span>  <br/> |<span data-ttu-id="dae1c-112">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dae1c-112">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dae1c-113">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dae1c-113">Row index:</span></span>  <br/> |<span data-ttu-id="dae1c-114">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="dae1c-114">**visRowEvent**</span></span> <br/> |
| <span data-ttu-id="dae1c-115">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dae1c-115">Cell index:</span></span>  <br/> |<span data-ttu-id="dae1c-116">**visEvtCellXFMod**</span><span class="sxs-lookup"><span data-stu-id="dae1c-116">**visEvtCellXFMod**</span></span> <br/> |
   

