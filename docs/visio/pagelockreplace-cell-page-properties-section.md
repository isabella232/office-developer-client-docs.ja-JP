---
title: '[PageLockReplace] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: このページで [図形の置換] ボタンを無効にするかどうかを示します。
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339481"
---
# <a name="pagelockreplace-cell-page-properties-section"></a><span data-ttu-id="0dd7f-103">[PageLockReplace] セル ([ページのプロパティ] セクション)</span><span class="sxs-lookup"><span data-stu-id="0dd7f-103">PageLockReplace Cell (Page Properties Section)</span></span>

<span data-ttu-id="0dd7f-104">このページで [**図形の置換**] ボタンを無効にするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="0dd7f-104">Indicates whether the **Replace Shape** button should be disabled for this page.</span></span> 
  
|<span data-ttu-id="0dd7f-105">**値**</span><span class="sxs-lookup"><span data-stu-id="0dd7f-105">**Value**</span></span>|<span data-ttu-id="0dd7f-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="0dd7f-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0dd7f-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="0dd7f-107">TRUE</span></span>  <br/> |<span data-ttu-id="0dd7f-108">このページがアクティブなとき、[**図形の変更**] ボタンは灰色表示されます。</span><span class="sxs-lookup"><span data-stu-id="0dd7f-108">The **Change Shape** button is grayed out when this page is active.</span></span>  <br/> |
|<span data-ttu-id="0dd7f-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="0dd7f-109">FALSE</span></span>  <br/> |<span data-ttu-id="0dd7f-110">このページによって [**図形の変更**] ボタンが無効になることはありません。</span><span class="sxs-lookup"><span data-stu-id="0dd7f-110">The **Change Shape** button is not disabled by this page.</span></span> <span data-ttu-id="0dd7f-111">**DocumentSheet** の **DocLockReplace** が **TRUE** に設定されている場合、または選択した図形の [**LockReplace**] セルが **TRUE** に設定されている場合は、このボタンが引き続き灰色表示される可能性があります。</span><span class="sxs-lookup"><span data-stu-id="0dd7f-111">The button may still be grayed out if: the **DocLockReplace** on the **DocumentSheet** is set to **TRUE**; the **LockReplace** cell for the selected shape is set to **TRUE**.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0dd7f-112">解説</span><span class="sxs-lookup"><span data-stu-id="0dd7f-112">Remarks</span></span>

<span data-ttu-id="0dd7f-113">別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**PageLockReplace**] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0dd7f-113">To get a reference to the **PageLockReplace** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0dd7f-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="0dd7f-114">Cell name:</span></span>  <br/> | <span data-ttu-id="0dd7f-115">[pagelockreplace]</span><span class="sxs-lookup"><span data-stu-id="0dd7f-115">PageLockReplace</span></span>  <br/> |
   
<span data-ttu-id="0dd7f-116">プログラムから、インデックスによって [**PageLockReplace**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0dd7f-116">To get a reference to the **PageLockReplace** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0dd7f-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0dd7f-117">Section index:</span></span>  <br/> |<span data-ttu-id="0dd7f-118">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0dd7f-118">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0dd7f-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0dd7f-119">Row index:</span></span>  <br/> |<span data-ttu-id="0dd7f-120">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="0dd7f-120">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="0dd7f-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0dd7f-121">Cell index:</span></span>  <br/> |<span data-ttu-id="0dd7f-122">**vispagelockreplace**</span><span class="sxs-lookup"><span data-stu-id="0dd7f-122">**visPageLockReplace**</span></span> <br/> |
   

