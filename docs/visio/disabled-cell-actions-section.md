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
ms.openlocfilehash: 3956b6cf5ccb870255d6943e74b4f02650952d09
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805222"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="cf081-103">[Disabled] セル ([操作] セクション)</span><span class="sxs-lookup"><span data-stu-id="cf081-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="cf081-104">ショートカット メニューまたはアクション タグ メニューの項目が使用不可であるかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="cf081-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="cf081-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="cf081-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="cf081-106">**値**</span><span class="sxs-lookup"><span data-stu-id="cf081-106">**Value**</span></span>|<span data-ttu-id="cf081-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="cf081-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="cf081-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="cf081-108">TRUE</span></span>  <br/> |<span data-ttu-id="cf081-109">コマンド名を無効 (灰色表示) にします。</span><span class="sxs-lookup"><span data-stu-id="cf081-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="cf081-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="cf081-110">FALSE</span></span>  <br/> |<span data-ttu-id="cf081-111">コマンド名を有効にします (既定値)。</span><span class="sxs-lookup"><span data-stu-id="cf081-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cf081-112">注釈</span><span class="sxs-lookup"><span data-stu-id="cf081-112">Remarks</span></span>

<span data-ttu-id="cf081-113">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [Disabled] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="cf081-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf081-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="cf081-114">Cell name:</span></span>  <br/> |<span data-ttu-id="cf081-115">アクションです。</span><span class="sxs-lookup"><span data-stu-id="cf081-115">Actions.</span></span> <span data-ttu-id="cf081-116">*名*です。無効になっているアクション。</span><span class="sxs-lookup"><span data-stu-id="cf081-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="cf081-117">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="cf081-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="cf081-118">プログラムから、インデックスによって [Disabled] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="cf081-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf081-119">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="cf081-119">Section index:</span></span>  <br/> |<span data-ttu-id="cf081-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="cf081-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="cf081-121">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="cf081-121">Row index:</span></span>  <br/> |<span data-ttu-id="cf081-122">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="cf081-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="cf081-123">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="cf081-123">Cell index:</span></span>  <br/> |<span data-ttu-id="cf081-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="cf081-124">**visActionDisabled**</span></span> <br/> |
   

