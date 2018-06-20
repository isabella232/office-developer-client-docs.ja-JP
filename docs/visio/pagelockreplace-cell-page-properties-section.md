---
title: '[PageLockReplace] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: このページの図形の置換] ボタンを無効にする必要があるかどうかを示します。
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805964"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="46e09-103">[PageLockReplace] セル ([ページのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="46e09-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="46e09-104">このページの**図形の置換**] ボタンを無効にする必要があるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="46e09-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="46e09-105">**値**</span><span class="sxs-lookup"><span data-stu-id="46e09-105">**Value**</span></span>|<span data-ttu-id="46e09-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="46e09-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="46e09-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="46e09-107">TRUE</span></span>  <br/> |<span data-ttu-id="46e09-108">このページがアクティブなときに、[**図形の変更**] ボタンは淡色表示されます。</span><span class="sxs-lookup"><span data-stu-id="46e09-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="46e09-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="46e09-109">FALSE</span></span>  <br/> |<span data-ttu-id="46e09-110">このページで、[**図形の変更**] ボタンが無効になっていません。</span><span class="sxs-lookup"><span data-stu-id="46e09-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="46e09-111">ボタンがまだ灰色場合: **DocumentSheet**の**DocLockReplace**になっている**場合は TRUE**です。選択した図形の**LockReplace**セルを**TRUE**に設定します。</span><span class="sxs-lookup"><span data-stu-id="46e09-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46e09-112">備考</span><span class="sxs-lookup"><span data-stu-id="46e09-112">Remarks</span></span>

<span data-ttu-id="46e09-113">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **PageLockReplace** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="46e09-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="46e09-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="46e09-114">Cell name:</span></span>  <br/> | <span data-ttu-id="46e09-115">PageLockReplace</span><span class="sxs-lookup"><span data-stu-id="46e09-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="46e09-116">プログラムから、インデックスによって [ **PageLockReplace** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="46e09-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="46e09-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="46e09-117">Section index:</span></span>  <br/> |<span data-ttu-id="46e09-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="46e09-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="46e09-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="46e09-119">Row index:</span></span>  <br/> |<span data-ttu-id="46e09-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="46e09-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="46e09-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="46e09-121">Cell index:</span></span>  <br/> |<span data-ttu-id="46e09-122">**visPageLockReplace**</span><span class="sxs-lookup"><span data-stu-id="46e09-122">**visPageLockReplace**</span></span> <br/> |
   

