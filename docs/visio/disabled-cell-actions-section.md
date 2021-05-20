---
title: '[Disabled] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431352"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="22066-103">[Disabled] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="22066-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="22066-104">ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="22066-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="22066-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="22066-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="22066-106">**値**</span><span class="sxs-lookup"><span data-stu-id="22066-106">**Value**</span></span>|<span data-ttu-id="22066-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="22066-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="22066-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="22066-108">TRUE</span></span>  <br/> |<span data-ttu-id="22066-109">コマンド名を無効 (灰色表示) にします。</span><span class="sxs-lookup"><span data-stu-id="22066-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="22066-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="22066-110">FALSE</span></span>  <br/> |<span data-ttu-id="22066-111">コマンド名を有効にします (既定値)。</span><span class="sxs-lookup"><span data-stu-id="22066-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="22066-112">注釈</span><span class="sxs-lookup"><span data-stu-id="22066-112">Remarks</span></span>

<span data-ttu-id="22066-113">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Disabled] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="22066-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22066-114">セル名 :</span><span class="sxs-lookup"><span data-stu-id="22066-114">Cell name:</span></span>  <br/> |<span data-ttu-id="22066-115">アクション。</span><span class="sxs-lookup"><span data-stu-id="22066-115">Actions.</span></span> <span data-ttu-id="22066-116">*name*  .[アクション] を無効にします。</span><span class="sxs-lookup"><span data-stu-id="22066-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="22066-117">*name*  は [アクション] 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="22066-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="22066-118">プログラムから、インデックスによって [Disabled] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="22066-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="22066-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="22066-119">Section index:</span></span>  <br/> |<span data-ttu-id="22066-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="22066-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="22066-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="22066-121">Row index:</span></span>  <br/> |<span data-ttu-id="22066-122">**visRowAction**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="22066-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="22066-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="22066-123">Cell index:</span></span>  <br/> |<span data-ttu-id="22066-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="22066-124">**visActionDisabled**</span></span> <br/> |
   

