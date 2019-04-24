---
title: '[FlyoutChild] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80003
localization_priority: Normal
ms.assetid: b2405457-843c-0d46-5f4f-9c413826c3f1
description: 行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。
ms.openlocfilehash: 85524ea33258449f5c9ee0991ac9a64f8f0eebae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346152"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="317d5-103">[FlyoutChild] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="317d5-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="317d5-104">行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="317d5-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="317d5-105">解説</span><span class="sxs-lookup"><span data-stu-id="317d5-105">Remarks</span></span>

<span data-ttu-id="317d5-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FlyoutChild] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="317d5-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="317d5-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="317d5-107">Cell name:</span></span>  <br/> |<span data-ttu-id="317d5-108">アクション.</span><span class="sxs-lookup"><span data-stu-id="317d5-108">Actions.</span></span> <span data-ttu-id="317d5-109">*名前*です。FlyoutChildwhere アクション。</span><span class="sxs-lookup"><span data-stu-id="317d5-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="317d5-110">*name*は、Actions 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="317d5-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="317d5-111">プログラムから、インデックスによって [FlyoutChild] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="317d5-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="317d5-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="317d5-112">Section index:</span></span>  <br/> |<span data-ttu-id="317d5-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="317d5-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="317d5-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="317d5-114">Row index:</span></span>  <br/> |<span data-ttu-id="317d5-115">**visRowAction** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="317d5-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="317d5-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="317d5-116">Cell index:</span></span>  <br/> |<span data-ttu-id="317d5-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="317d5-117">**visActionFlyoutChild**</span></span> <br/> |
   

