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
ms.openlocfilehash: 8749b7d6db4a932b97c68ab5cf30b879a57d28f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805593"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="51c30-103">[Invisible] セル ([操作] セクション)</span><span class="sxs-lookup"><span data-stu-id="51c30-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="51c30-104">アクション タグ メニューまたはショートカット メニューに、アクションを表示するかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="51c30-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="51c30-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="51c30-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="51c30-106">**値**</span><span class="sxs-lookup"><span data-stu-id="51c30-106">**Value**</span></span>|<span data-ttu-id="51c30-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="51c30-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="51c30-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="51c30-108">TRUE</span></span>  <br/> |<span data-ttu-id="51c30-109">アクションはメニューに表示されません。</span><span class="sxs-lookup"><span data-stu-id="51c30-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="51c30-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="51c30-110">FALSE</span></span>  <br/> |<span data-ttu-id="51c30-111">アクションはメニューに表示されます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="51c30-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="51c30-112">注釈</span><span class="sxs-lookup"><span data-stu-id="51c30-112">Remarks</span></span>

<span data-ttu-id="51c30-113">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Invisible] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="51c30-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51c30-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="51c30-114">Cell name:</span></span>  <br/> |<span data-ttu-id="51c30-115">アクションです。</span><span class="sxs-lookup"><span data-stu-id="51c30-115">Actions.</span></span> <span data-ttu-id="51c30-116">*名*です。Invisiblewhere アクションです。</span><span class="sxs-lookup"><span data-stu-id="51c30-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="51c30-117">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="51c30-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="51c30-118">プログラムから、インデックスによって [Invisible] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="51c30-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="51c30-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="51c30-119">Section index:</span></span>  <br/> |<span data-ttu-id="51c30-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="51c30-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="51c30-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="51c30-121">Row index:</span></span>  <br/> |<span data-ttu-id="51c30-122">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="51c30-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="51c30-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="51c30-123">Cell index:</span></span>  <br/> |<span data-ttu-id="51c30-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="51c30-124">**visActionInvisible**</span></span> <br/> |
   

