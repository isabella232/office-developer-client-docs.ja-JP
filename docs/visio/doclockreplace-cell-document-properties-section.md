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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413424"
---
# <a name="doclockreplace-cell-document-properties-section"></a><span data-ttu-id="0d55e-103">[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="0d55e-103">DocLockReplace Cell (Document Properties Section)</span></span>

<span data-ttu-id="0d55e-104">置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="0d55e-104">Determines whether the replace shape UI should be disabled for this document.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0d55e-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="0d55e-105">TRUE</span></span>  <br/> |<span data-ttu-id="0d55e-106">UI の [**図形の置換**] ボタンは灰色表示されます。</span><span class="sxs-lookup"><span data-stu-id="0d55e-106">The **Replace Shape** button is grayed out in the UI.</span></span>  <br/> |
|<span data-ttu-id="0d55e-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="0d55e-107">FALSE</span></span>  <br/> |<span data-ttu-id="0d55e-p101">UI の [**図形の置換**] ボタンはアクティブです。ユーザーはこのドキュメントで [図形の置換] 機能を使用できます。図形の置換</span><span class="sxs-lookup"><span data-stu-id="0d55e-p101">The **Replace Shape** button is active in the UI. Users can use the Replace Shape feature in this document.  </span></span><br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d55e-110">注釈</span><span class="sxs-lookup"><span data-stu-id="0d55e-110">Remarks</span></span>

<span data-ttu-id="0d55e-111">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**DocLockReplace**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0d55e-111">To get a reference to the **DocLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d55e-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="0d55e-112">Cell name:</span></span>  <br/> | <span data-ttu-id="0d55e-113">doclocreplace</span><span class="sxs-lookup"><span data-stu-id="0d55e-113">DocLocReplace</span></span>  <br/> |
   
<span data-ttu-id="0d55e-114">プログラムから、インデックスによって [**DocLocReplace**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0d55e-114">To get a reference to the **DocLocReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0d55e-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d55e-115">Section index:</span></span>  <br/> |<span data-ttu-id="0d55e-116">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0d55e-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0d55e-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d55e-117">Row index:</span></span>  <br/> |<span data-ttu-id="0d55e-118">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="0d55e-118">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="0d55e-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0d55e-119">Cell index:</span></span>  <br/> |<span data-ttu-id="0d55e-120">\* \* visDocLockReplace \* \*</span><span class="sxs-lookup"><span data-stu-id="0d55e-120">\*\*visDocLockReplace \*\*</span></span> <br/> |
   

