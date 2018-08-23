---
title: '[TagName] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: このアクションに関連付けられているアクション タグの名前を指定します。
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806619"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="3acd1-103">[TagName ] セル ([操作] セクション)</span><span class="sxs-lookup"><span data-stu-id="3acd1-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="3acd1-104">このアクションに関連付けられているアクション タグの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="3acd1-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="3acd1-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="3acd1-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="3acd1-106">注釈</span><span class="sxs-lookup"><span data-stu-id="3acd1-106">Remarks</span></span>

<span data-ttu-id="3acd1-107">[Actions] セクションの [TagName] セルは、[Action Tags] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。</span><span class="sxs-lookup"><span data-stu-id="3acd1-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="3acd1-108">アクションの行の [tagname] セルが空白の場合、[操作] メニューのタグではなく、ショートカット メニューのアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3acd1-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="3acd1-109">アクション行の [tagname] セルの値には、スマート タグ行の [tagname] セルの値が一致すると、アクションを [アクション] メニューのタグが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3acd1-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="3acd1-110">アクションの [tagname] セルが値を持つタグ行の [tagname] の値に一致しない場合は、そのアクションは任意のアクション タグのメニューまたはショートカット メニューに表示されません。</span><span class="sxs-lookup"><span data-stu-id="3acd1-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="3acd1-111">いくつかのスマート タグ行の [TagName] の値が同じ場合、すべてに同じアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="3acd1-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="3acd1-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="3acd1-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3acd1-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="3acd1-113">Cell name:</span></span>  <br/> |<span data-ttu-id="3acd1-114">アクションです。</span><span class="sxs-lookup"><span data-stu-id="3acd1-114">Actions.</span></span> <span data-ttu-id="3acd1-115">*名*です。TagNamewhere アクションです。</span><span class="sxs-lookup"><span data-stu-id="3acd1-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="3acd1-116">*アクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="3acd1-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="3acd1-117">プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="3acd1-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3acd1-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="3acd1-118">Section index:</span></span>  <br/> |<span data-ttu-id="3acd1-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="3acd1-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="3acd1-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="3acd1-120">Row index:</span></span>  <br/> |<span data-ttu-id="3acd1-121">**visRowAction** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="3acd1-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="3acd1-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="3acd1-122">Cell index:</span></span>  <br/> |<span data-ttu-id="3acd1-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="3acd1-123">**visActionTagName**</span></span> <br/> |
   

