---
title: '[ReadOnly] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434236"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="4ee00-103">[ReadOnly] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="4ee00-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="4ee00-104">ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="4ee00-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4ee00-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="4ee00-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="4ee00-106">**値**</span><span class="sxs-lookup"><span data-stu-id="4ee00-106">**Value**</span></span>|<span data-ttu-id="4ee00-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="4ee00-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4ee00-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="4ee00-108">TRUE</span></span>  <br/> |<span data-ttu-id="4ee00-109">アクションはメニューに表示されますが、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="4ee00-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="4ee00-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="4ee00-110">FALSE</span></span>  <br/> |<span data-ttu-id="4ee00-111">アクションはメニューに表示され、選択できます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="4ee00-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4ee00-112">注釈</span><span class="sxs-lookup"><span data-stu-id="4ee00-112">Remarks</span></span>

<span data-ttu-id="4ee00-113">アクションが読み取り専用の場合、アクション タグ メニューまたはショートカット メニューに表示されますが、選択できません。</span><span class="sxs-lookup"><span data-stu-id="4ee00-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="4ee00-114">灰色表示にはなりませんが、色が付いた背景の上にラベルのように表示されます。</span><span class="sxs-lookup"><span data-stu-id="4ee00-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="4ee00-115">そのメニュー項目を灰色表示にするには、[Disabled] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="4ee00-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="4ee00-116">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [ReadOnly] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4ee00-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ee00-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="4ee00-117">Cell name:</span></span>  <br/> |<span data-ttu-id="4ee00-118">アクション。</span><span class="sxs-lookup"><span data-stu-id="4ee00-118">Actions.</span></span> <span data-ttu-id="4ee00-119">*name*  .ReadOnlywhere Actions.</span><span class="sxs-lookup"><span data-stu-id="4ee00-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="4ee00-120">*name*  は [アクション] 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="4ee00-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="4ee00-121">プログラムから、インデックスによって [ReadOnly] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4ee00-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4ee00-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ee00-122">Section index:</span></span>  <br/> |<span data-ttu-id="4ee00-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="4ee00-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="4ee00-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ee00-124">Row index:</span></span>  <br/> |<span data-ttu-id="4ee00-125">**visRowAction**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4ee00-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="4ee00-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4ee00-126">Cell index:</span></span>  <br/> |<span data-ttu-id="4ee00-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="4ee00-127">**visActionReadOnly**</span></span> <br/> |
   

