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
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806145"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="605b8-103">[ReadOnly] セル ([操作] セクション)</span><span class="sxs-lookup"><span data-stu-id="605b8-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="605b8-104">ショートカット メニューまたはアクション タグ メニューのアクションを読み取り専用にするかどうかを制御します。</span><span class="sxs-lookup"><span data-stu-id="605b8-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="605b8-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="605b8-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="605b8-106">**値**</span><span class="sxs-lookup"><span data-stu-id="605b8-106">**Value**</span></span>|<span data-ttu-id="605b8-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="605b8-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="605b8-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="605b8-108">TRUE</span></span>  <br/> |<span data-ttu-id="605b8-109">アクションはメニューに表示されますが、読み取り専用です。</span><span class="sxs-lookup"><span data-stu-id="605b8-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="605b8-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="605b8-110">FALSE</span></span>  <br/> |<span data-ttu-id="605b8-111">アクションはメニューに表示され、選択できます (既定値)。</span><span class="sxs-lookup"><span data-stu-id="605b8-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="605b8-112">注釈</span><span class="sxs-lookup"><span data-stu-id="605b8-112">Remarks</span></span>

<span data-ttu-id="605b8-113">読み取り専用操作では、アクションのタグやショートカット メニューに表示されますがそれを選択することはできません。</span><span class="sxs-lookup"><span data-stu-id="605b8-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="605b8-114">淡色表示されますが、ラベルのように、色付きの背景に表示されます。</span><span class="sxs-lookup"><span data-stu-id="605b8-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="605b8-115">メニュー項目が淡色表示にするには、無効なセルを使用します。</span><span class="sxs-lookup"><span data-stu-id="605b8-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="605b8-116">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [ReadOnly] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="605b8-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="605b8-117">セル名:</span><span class="sxs-lookup"><span data-stu-id="605b8-117">Cell name:</span></span>  <br/> |<span data-ttu-id="605b8-118">アクションです。</span><span class="sxs-lookup"><span data-stu-id="605b8-118">Actions.</span></span> <span data-ttu-id="605b8-119">*名*です。ReadOnlywhere アクションです。</span><span class="sxs-lookup"><span data-stu-id="605b8-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="605b8-120">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="605b8-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="605b8-121">プログラムから、インデックスによって [ReadOnly] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="605b8-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="605b8-122">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="605b8-122">Section index:</span></span>  <br/> |<span data-ttu-id="605b8-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="605b8-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="605b8-124">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="605b8-124">Row index:</span></span>  <br/> |<span data-ttu-id="605b8-125">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="605b8-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="605b8-126">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="605b8-126">Cell index:</span></span>  <br/> |<span data-ttu-id="605b8-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="605b8-127">**visActionReadOnly**</span></span> <br/> |
   

