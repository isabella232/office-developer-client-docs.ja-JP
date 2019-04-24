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
ms.openlocfilehash: 665130e9f9f938349028ffa1d1c06224e746de5d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335323"
---
# <a name="inhibitsnap-cell-page-properties-section"></a><span data-ttu-id="dca24-103">[InhibitSnap] セル ([Page Properties] セクション)</span><span class="sxs-lookup"><span data-stu-id="dca24-103">InhibitSnap Cell (Page Properties Section)</span></span>

<span data-ttu-id="dca24-104">前景ページ上の図形を、同じページにある他のオブジェクトや背景ページ上の図形にスナップするかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="dca24-104">Determines whether the shapes on a foreground page snap to other objects on the page and shapes on the background page.</span></span>
  
|<span data-ttu-id="dca24-105">**値**</span><span class="sxs-lookup"><span data-stu-id="dca24-105">**Value**</span></span>|<span data-ttu-id="dca24-106">**説明**</span><span class="sxs-lookup"><span data-stu-id="dca24-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dca24-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="dca24-107">TRUE</span></span>  <br/> | <span data-ttu-id="dca24-108">ページ上のスナップ操作をすべて無効にします。ただし、ルーラーとグリッドへのスナップは除きます。</span><span class="sxs-lookup"><span data-stu-id="dca24-108">Inhibit all snapping on the page, except for snapping to the ruler and grid.</span></span>  <br/> |
| <span data-ttu-id="dca24-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="dca24-109">FALSE</span></span>  <br/> | <span data-ttu-id="dca24-110">スナップ操作を有効にします。</span><span class="sxs-lookup"><span data-stu-id="dca24-110">Enable snapping.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dca24-111">解説</span><span class="sxs-lookup"><span data-stu-id="dca24-111">Remarks</span></span>

<span data-ttu-id="dca24-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [InhibitSnap] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="dca24-112">To get a reference to the InhibitSnap cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dca24-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="dca24-113">Cell name:</span></span>  <br/> | <span data-ttu-id="dca24-114">[inhibitsnap]</span><span class="sxs-lookup"><span data-stu-id="dca24-114">InhibitSnap</span></span>  <br/> |
   
<span data-ttu-id="dca24-115">プログラムから、インデックスによって [InhibitSnap] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="dca24-115">To get a reference to the InhibitSnap cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dca24-116">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="dca24-116">Section index:</span></span>  <br/> |<span data-ttu-id="dca24-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="dca24-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="dca24-118">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="dca24-118">Row index:</span></span>  <br/> |<span data-ttu-id="dca24-119">**visRowPage**</span><span class="sxs-lookup"><span data-stu-id="dca24-119">**visRowPage**</span></span> <br/> |
| <span data-ttu-id="dca24-120">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="dca24-120">Cell index:</span></span>  <br/> |<span data-ttu-id="dca24-121">**visPageInhibitSnap**</span><span class="sxs-lookup"><span data-stu-id="dca24-121">**visPageInhibitSnap**</span></span> <br/> |
   

