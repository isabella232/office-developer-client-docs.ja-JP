---
title: '[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: 置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338606"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="3b9c4-103">[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="3b9c4-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="3b9c4-104">置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="3b9c4-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3b9c4-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="3b9c4-105">TRUE</span></span>  <br/> |<span data-ttu-id="3b9c4-106">UI の [**図形の置換**] ボタンは灰色表示されます。</span><span class="sxs-lookup"><span data-stu-id="3b9c4-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="3b9c4-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="3b9c4-107">FALSE</span></span>  <br/> |<span data-ttu-id="3b9c4-p101">UI の [**図形の置換**] ボタンはアクティブです。ユーザーはこのドキュメントで [図形の置換] 機能を使用できます。図形の置換</span><span class="sxs-lookup"><span data-stu-id="3b9c4-p101">The **Replace Shape** button is active in the UI. Users can use the Replace Shape feature in this document.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b9c4-110">解説</span><span class="sxs-lookup"><span data-stu-id="3b9c4-110">Remarks</span></span>

<span data-ttu-id="3b9c4-111">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**DocLockReplace**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3b9c4-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b9c4-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="3b9c4-112">Cell name:</span></span>  <br/> | <span data-ttu-id="3b9c4-113">doclocreplace</span><span class="sxs-lookup"><span data-stu-id="3b9c4-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="3b9c4-114">プログラムから、インデックスによって [**DocLocReplace**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3b9c4-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b9c4-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b9c4-115">Section index:</span></span>  <br/> |<span data-ttu-id="3b9c4-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3b9c4-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3b9c4-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b9c4-117">Row index:</span></span>  <br/> |<span data-ttu-id="3b9c4-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="3b9c4-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="3b9c4-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3b9c4-119">Cell index:</span></span>  <br/> |<span data-ttu-id="3b9c4-120">\* \* visDocLockReplace \* \*</span><span class="sxs-lookup"><span data-stu-id="3b9c4-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

