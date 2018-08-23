---
title: '[DocLockDuplicatePage] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805247"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a><span data-ttu-id="5dfc7-103">[DocLockDuplicatePage] セル ([ドキュメントのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="5dfc7-103">DocLockDuplicatePage Cell (Document Properties Section)</span></span>

<span data-ttu-id="5dfc7-104">ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。</span><span class="sxs-lookup"><span data-stu-id="5dfc7-104">Determines whether pages in the document can be duplicated, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="5dfc7-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="5dfc7-105">TRUE</span></span>  <br/> |<span data-ttu-id="5dfc7-106">ページのショートカット メニューの  [**複製**] と、**Page.Duplicate** オートメーション メソッドはどちらも無効化されています。</span><span class="sxs-lookup"><span data-stu-id="5dfc7-106">**Duplicate** in the page shortcut menu and the **Page.Duplicate** automation method are both disabled.</span></span>  <br/> |
|<span data-ttu-id="5dfc7-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="5dfc7-107">FALSE</span></span>  <br/> |<span data-ttu-id="5dfc7-108">このページは複製できます。</span><span class="sxs-lookup"><span data-stu-id="5dfc7-108">The page can be duplicated.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5dfc7-109">Remarks</span><span class="sxs-lookup"><span data-stu-id="5dfc7-109">Remarks</span></span>

<span data-ttu-id="5dfc7-110">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**DocLockDuplicatePage**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="5dfc7-110">To get a reference to the **DocLockDuplicatePage** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5dfc7-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="5dfc7-111">Cell name:</span></span>  <br/> | <span data-ttu-id="5dfc7-112">DocLockDuplicatePage</span><span class="sxs-lookup"><span data-stu-id="5dfc7-112">DocLockDuplicatePage</span></span>  <br/> |
   
<span data-ttu-id="5dfc7-113">プログラムから、インデックスによって [**DocLockDuplicatePage**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="5dfc7-113">To get a reference to the **DocLockDuplicatePage** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5dfc7-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="5dfc7-114">Section index:</span></span>  <br/> |<span data-ttu-id="5dfc7-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5dfc7-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5dfc7-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="5dfc7-116">Row index:</span></span>  <br/> |<span data-ttu-id="5dfc7-117">**visRowDoc**</span><span class="sxs-lookup"><span data-stu-id="5dfc7-117">**visRowDoc**</span></span> <br/> |
| <span data-ttu-id="5dfc7-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="5dfc7-118">Cell index:</span></span>  <br/> |<span data-ttu-id="5dfc7-119">**visDocLockDuplicatePage**</span><span class="sxs-lookup"><span data-stu-id="5dfc7-119">**visDocLockDuplicatePage**</span></span> <br/> |
   

