---
title: '[Invisible] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297243"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="a15c0-103">[Invisible] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="a15c0-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="a15c0-104">アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="a15c0-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a15c0-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="a15c0-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="a15c0-106">**値**</span><span class="sxs-lookup"><span data-stu-id="a15c0-106">**Value**</span></span>|<span data-ttu-id="a15c0-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="a15c0-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a15c0-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="a15c0-108">TRUE</span></span>  <br/> |<span data-ttu-id="a15c0-109">アクションはメニューに表示されません。</span><span class="sxs-lookup"><span data-stu-id="a15c0-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="a15c0-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="a15c0-110">FALSE</span></span>  <br/> |<span data-ttu-id="a15c0-111">アクションはメニューに表示されます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="a15c0-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a15c0-112">解説</span><span class="sxs-lookup"><span data-stu-id="a15c0-112">Remarks</span></span>

<span data-ttu-id="a15c0-113">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a15c0-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a15c0-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="a15c0-114">Cell name:</span></span>  <br/> |<span data-ttu-id="a15c0-115">アクション.</span><span class="sxs-lookup"><span data-stu-id="a15c0-115">Actions.</span></span> <span data-ttu-id="a15c0-116">*名前*です。Invisiblewhere アクション。</span><span class="sxs-lookup"><span data-stu-id="a15c0-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="a15c0-117">*name*は、Actions 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="a15c0-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a15c0-118">プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a15c0-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a15c0-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a15c0-119">Section index:</span></span>  <br/> |<span data-ttu-id="a15c0-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a15c0-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a15c0-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a15c0-121">Row index:</span></span>  <br/> |<span data-ttu-id="a15c0-122">**visRowAction** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="a15c0-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a15c0-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a15c0-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a15c0-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="a15c0-124">**visActionInvisible**</span></span> <br/> |
   

