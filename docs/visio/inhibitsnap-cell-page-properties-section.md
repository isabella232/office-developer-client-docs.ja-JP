---
title: '[InhibitSnap] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251620
localization_priority: Normal
ms.assetid: ab9fcebc-1550-3b9e-e3b4-e8b92424390b
description: 前景ページ上の図形を、同じページにある他のオブジェクトや背景ページ上の図形にスナップするかどうかを指定します。
ms.openlocfilehash: b95dafda9ebef36db34f60585ab3ed2164ade415
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805585"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="c112d-103">[InhibitSnap] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="c112d-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="c112d-104">前景ページ上の図形を、同じページにある他のオブジェクトや背景ページ上の図形にスナップするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="c112d-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="c112d-105">**値**</span><span class="sxs-lookup"><span data-stu-id="c112d-105">**Value**</span></span>|<span data-ttu-id="c112d-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="c112d-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="c112d-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="c112d-107">TRUE</span></span>  <br/> | <span data-ttu-id="c112d-108">ページ上のスナップ操作をすべて無効にします。ただし、ルーラーとグリッドへのスナップは除きます。</span><span class="sxs-lookup"><span data-stu-id="c112d-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="c112d-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="c112d-109">FALSE</span></span>  <br/> | <span data-ttu-id="c112d-110">スナップ操作を有効にします。</span><span class="sxs-lookup"><span data-stu-id="c112d-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c112d-111">備考</span><span class="sxs-lookup"><span data-stu-id="c112d-111">Remarks</span></span>

<span data-ttu-id="c112d-112">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[InhibitSnap] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="c112d-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c112d-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="c112d-113">Cell name:</span></span>  <br/> | <span data-ttu-id="c112d-114">InhibitSnap</span><span class="sxs-lookup"><span data-stu-id="c112d-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="c112d-115">プログラムから、インデックスによって [InhibitSnap] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="c112d-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c112d-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="c112d-116">Section index:</span></span>  <br/> |<span data-ttu-id="c112d-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c112d-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c112d-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="c112d-118">Row index:</span></span>  <br/> |<span data-ttu-id="c112d-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="c112d-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="c112d-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="c112d-120">Cell index:</span></span>  <br/> |<span data-ttu-id="c112d-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="c112d-121">**visPageInhibitSnap**</span></span> <br/> |
   

