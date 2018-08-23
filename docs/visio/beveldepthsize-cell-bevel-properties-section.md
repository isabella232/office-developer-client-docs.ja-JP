---
title: '[BevelDepthSize] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c6a57e52-c7ed-4a52-940f-1cef9baa70a5
description: 傾斜面の深さをポイント単位でのサイズを決定します。
ms.openlocfilehash: 4b6f686b0afe1c09411435797cadc6f93fa0938f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804822"
---
# <a name="beveldepthsize-cell-bevel-properties-section"></a><span data-ttu-id="a7712-103">[BevelDepthSize] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="a7712-103">BevelDepthSize Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="a7712-104">傾斜面の深さをポイント単位でのサイズを決定します。</span><span class="sxs-lookup"><span data-stu-id="a7712-104">Determines the size of the bevel's depth in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a7712-105">注釈</span><span class="sxs-lookup"><span data-stu-id="a7712-105">Remarks</span></span>

<span data-ttu-id="a7712-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelDepthSize** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="a7712-106">To get a reference to the **BevelDepthSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a7712-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="a7712-107">Cell name:</span></span>  <br/> | <span data-ttu-id="a7712-108">BevelDepthSize</span><span class="sxs-lookup"><span data-stu-id="a7712-108">BevelDepthSize</span></span>  <br/> |
   
<span data-ttu-id="a7712-109">プログラムから、インデックスによって [ **BevelDepthSize** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="a7712-109">To get a reference to the **BevelDepthSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a7712-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a7712-110">Section index:</span></span>  <br/> |<span data-ttu-id="a7712-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="a7712-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="a7712-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a7712-112">Row index:</span></span>  <br/> |<span data-ttu-id="a7712-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="a7712-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="a7712-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a7712-114">Cell index:</span></span>  <br/> |<span data-ttu-id="a7712-115">**visBevelDepthSize**</span><span class="sxs-lookup"><span data-stu-id="a7712-115">**visBevelDepthSize**</span></span> <br/> |
   

