---
title: '[EventMultiDrop] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337192"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="5b222-102">[EventMultiDrop] セル ([Events] セクション)</span><span class="sxs-lookup"><span data-stu-id="5b222-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="5b222-103">図面ページに複数の図形をインスタンスとしてドロップしたとき、または図形を複製または貼り付けたときに評価されるイベントセルです。</span><span class="sxs-lookup"><span data-stu-id="5b222-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="5b222-104">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="5b222-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="5b222-105">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventMultiDrop] セルを参照するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5b222-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b222-106">セル名:</span><span class="sxs-lookup"><span data-stu-id="5b222-106">Cell name:</span></span>  <br/> |<span data-ttu-id="5b222-107">[eventmultidrop]</span><span class="sxs-lookup"><span data-stu-id="5b222-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="5b222-108">プログラムから、インデックスによって [EventMultiDrop] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b222-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5b222-109">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b222-109">Section index:</span></span>  <br/> |<span data-ttu-id="5b222-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5b222-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="5b222-111">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b222-111">Row index:</span></span>  <br/> |<span data-ttu-id="5b222-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="5b222-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="5b222-113">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5b222-113">Cell index:</span></span>  <br/> |<span data-ttu-id="5b222-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="5b222-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

