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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359991"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="9fa29-103">[ReadOnly] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="9fa29-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="9fa29-104">ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="9fa29-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9fa29-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="9fa29-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="9fa29-106">**値**</span><span class="sxs-lookup"><span data-stu-id="9fa29-106">**Value**</span></span>|<span data-ttu-id="9fa29-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="9fa29-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9fa29-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="9fa29-108">TRUE</span></span>  <br/> |<span data-ttu-id="9fa29-109">アクションはメニューに表示されますが、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="9fa29-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="9fa29-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="9fa29-110">FALSE</span></span>  <br/> |<span data-ttu-id="9fa29-111">アクションはメニューに表示され、選択できます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="9fa29-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9fa29-112">解説</span><span class="sxs-lookup"><span data-stu-id="9fa29-112">Remarks</span></span>

<span data-ttu-id="9fa29-113">アクションが読み取り専用の場合、アクション タグ メニューまたはショートカット メニューに表示されますが、選択できません。</span><span class="sxs-lookup"><span data-stu-id="9fa29-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="9fa29-114">灰色表示にはなりませんが、色が付いた背景の上にラベルのように表示されます。</span><span class="sxs-lookup"><span data-stu-id="9fa29-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="9fa29-115">そのメニュー項目を灰色表示にするには、[Disabled] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="9fa29-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="9fa29-116">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [ReadOnly] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="9fa29-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fa29-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="9fa29-117">Cell name:</span></span>  <br/> |<span data-ttu-id="9fa29-118">アクション.</span><span class="sxs-lookup"><span data-stu-id="9fa29-118">Actions.</span></span> <span data-ttu-id="9fa29-119">*名前*です。ReadOnlywhere アクション。</span><span class="sxs-lookup"><span data-stu-id="9fa29-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="9fa29-120">*name*は、Actions 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="9fa29-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="9fa29-121">プログラムから、インデックスによって [ReadOnly] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="9fa29-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9fa29-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fa29-122">Section index:</span></span>  <br/> |<span data-ttu-id="9fa29-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="9fa29-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="9fa29-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fa29-124">Row index:</span></span>  <br/> |<span data-ttu-id="9fa29-125">**visRowAction** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="9fa29-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9fa29-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="9fa29-126">Cell index:</span></span>  <br/> |<span data-ttu-id="9fa29-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="9fa29-127">**visActionReadOnly**</span></span> <br/> |
   

