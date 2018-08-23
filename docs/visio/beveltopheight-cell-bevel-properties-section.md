---
title: '[BevelTopHeight] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b09b48d0-9008-4e43-9506-93a830ad9452
description: ポイントで図形の上の面取りの高さを決定します。
ms.openlocfilehash: 09aefb15118a2a443418b3193dbbebf6d8532c3e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804831"
---
# <a name="beveltopheight-cell-bevel-properties-section"></a><span data-ttu-id="3f9dc-103">[BevelTopHeight] セル ([ベベルのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="3f9dc-103">BevelTopHeight Cell (Bevel Properties Section)</span></span>

<span data-ttu-id="3f9dc-104">ポイントで図形の上の面取りの高さを決定します。</span><span class="sxs-lookup"><span data-stu-id="3f9dc-104">Determines the height of a shape's top bevel in points.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3f9dc-105">注釈</span><span class="sxs-lookup"><span data-stu-id="3f9dc-105">Remarks</span></span>

<span data-ttu-id="3f9dc-106">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelTopHeight** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="3f9dc-106">To get a reference to the **BevelTopHeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f9dc-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="3f9dc-107">Cell name:</span></span>  <br/> | <span data-ttu-id="3f9dc-108">BevelTopHeight</span><span class="sxs-lookup"><span data-stu-id="3f9dc-108">BevelTopHeight</span></span>  <br/> |
   
<span data-ttu-id="3f9dc-109">プログラムから、インデックスによって [ **BevelTopHeight** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="3f9dc-109">To get a reference to the **BevelTopHeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3f9dc-110">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f9dc-110">Section index:</span></span>  <br/> |<span data-ttu-id="3f9dc-111">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3f9dc-111">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3f9dc-112">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f9dc-112">Row index:</span></span>  <br/> |<span data-ttu-id="3f9dc-113">**visRowBevelProperties**</span><span class="sxs-lookup"><span data-stu-id="3f9dc-113">**visRowBevelProperties**</span></span> <br/> |
| <span data-ttu-id="3f9dc-114">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3f9dc-114">Cell index:</span></span>  <br/> |<span data-ttu-id="3f9dc-115">**visBevelTopHeight**</span><span class="sxs-lookup"><span data-stu-id="3f9dc-115">**visBevelTopHeight**</span></span> <br/> |
   

