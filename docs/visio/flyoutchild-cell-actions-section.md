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
ms.openlocfilehash: 8a41721f91fa9632246e512cfd4ba1a2d871ece5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805407"
---
# <a name="flyoutchild-cell-actions-section"></a><span data-ttu-id="57c20-103">[FlyoutChild] セル ([操作] セクション)</span><span class="sxs-lookup"><span data-stu-id="57c20-103">FlyoutChild Cell (Actions Section)</span></span>

<span data-ttu-id="57c20-104">行が、サブ項目の子ではない行の上の最終行の子サブ項目メニューかどうかを指定します。</span><span class="sxs-lookup"><span data-stu-id="57c20-104">Determines whether the row is a child flyout menu of the last row above it that is not a flyout child.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="57c20-105">注釈</span><span class="sxs-lookup"><span data-stu-id="57c20-105">Remarks</span></span>

<span data-ttu-id="57c20-106">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FlyoutChild] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="57c20-106">To get a reference to the FlyoutChild cell by name from another formula, or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57c20-107">セル名:</span><span class="sxs-lookup"><span data-stu-id="57c20-107">Cell name:</span></span>  <br/> |<span data-ttu-id="57c20-108">アクションです。</span><span class="sxs-lookup"><span data-stu-id="57c20-108">Actions.</span></span> <span data-ttu-id="57c20-109">*名*です。FlyoutChildwhere アクションです。</span><span class="sxs-lookup"><span data-stu-id="57c20-109">*name*  .FlyoutChildwhere Actions.</span></span>  <span data-ttu-id="57c20-110">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="57c20-110">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="57c20-111">プログラムから、インデックスによって [FlyoutChild] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="57c20-111">To get a reference to the FlyoutChild cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="57c20-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="57c20-112">Section index:</span></span>  <br/> |<span data-ttu-id="57c20-113">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="57c20-113">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="57c20-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="57c20-114">Row index:</span></span>  <br/> |<span data-ttu-id="57c20-115">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="57c20-115">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="57c20-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="57c20-116">Cell index:</span></span>  <br/> |<span data-ttu-id="57c20-117">**visActionFlyoutChild**</span><span class="sxs-lookup"><span data-stu-id="57c20-117">**visActionFlyoutChild**</span></span> <br/> |
   

