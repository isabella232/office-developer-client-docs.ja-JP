---
title: '[EventMultiDrop] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805338"
---
# <a name="eventmultidrop-cell-events-section"></a><span data-ttu-id="0c2dd-102">[EventMultiDrop] セル ([イベント] セクション)</span><span class="sxs-lookup"><span data-stu-id="0c2dd-102">EventMultiDrop Cell (Events Section)</span></span>

<span data-ttu-id="0c2dd-103">インスタンスまたはシェイプを複製したり貼り付けたときに、図面ページに複数の図形をドロップしたときに評価されるイベント セルです。</span><span class="sxs-lookup"><span data-stu-id="0c2dd-103">An event cell that is evaluated when multiple shapes are dropped on the drawing page, either as instances or when shapes are duplicated or pasted.</span></span>
  
<span data-ttu-id="0c2dd-104">イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。</span><span class="sxs-lookup"><span data-stu-id="0c2dd-104">Event cells are evaluated only when the event occurs, not upon formula entry.</span></span>
  
<span data-ttu-id="0c2dd-105">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventMultiDrop] セルを参照するには、次の値を使用します。

</span><span class="sxs-lookup"><span data-stu-id="0c2dd-105">To refer to the EventMultiDrop cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c2dd-106">セル名:</span><span class="sxs-lookup"><span data-stu-id="0c2dd-106">Cell name:</span></span>  <br/> |<span data-ttu-id="0c2dd-107">EventMultiDrop</span><span class="sxs-lookup"><span data-stu-id="0c2dd-107">EventMultiDrop</span></span>  <br/> |
   
<span data-ttu-id="0c2dd-108">プログラムから、インデックスによって [EventMultiDrop] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。

</span><span class="sxs-lookup"><span data-stu-id="0c2dd-108">To refer to the EventMultiDrop cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0c2dd-109">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c2dd-109">Section index:</span></span>  <br/> |<span data-ttu-id="0c2dd-110">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-110">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="0c2dd-111">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c2dd-111">Row index:</span></span>  <br/> |<span data-ttu-id="0c2dd-112">**visRowEvent**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-112">**visRowEvent**</span></span> <br/> |
|<span data-ttu-id="0c2dd-113">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0c2dd-113">Cell index:</span></span>  <br/> |<span data-ttu-id="0c2dd-114">**visEvtCellMultiDrop**</span><span class="sxs-lookup"><span data-stu-id="0c2dd-114">**visEvtCellMultiDrop**</span></span> <br/> |
   

