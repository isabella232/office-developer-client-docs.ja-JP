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
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412717"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="98b89-103">[TagName] セル ([Actions] セクション)</span><span class="sxs-lookup"><span data-stu-id="98b89-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="98b89-104">このアクションに関連付けられているアクション タグの名前を指定します。</span><span class="sxs-lookup"><span data-stu-id="98b89-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="98b89-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="98b89-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="98b89-106">注釈</span><span class="sxs-lookup"><span data-stu-id="98b89-106">Remarks</span></span>

<span data-ttu-id="98b89-107">[Actions] セクションの [TagName] セルは、[Action Tags] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。</span><span class="sxs-lookup"><span data-stu-id="98b89-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="98b89-108">[Actions] 行の [TagName] セルが空白の場合は、アクションタグメニューではなく、ショートカットメニューにアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="98b89-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="98b89-109">[Actions] 行の [tagname] セル値が [Smart Tags] 行の [tagname] セル値と一致する場合、アクションはアクションタグメニューに表示されます。</span><span class="sxs-lookup"><span data-stu-id="98b89-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="98b89-110">アクションの [tagname] セルに値があっても、どの図形タグ行の [tagname] の値と一致しない場合、そのアクションはアクションタグメニューまたはショートカットメニューに表示されません。</span><span class="sxs-lookup"><span data-stu-id="98b89-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="98b89-111">いくつかのスマート タグ行の [TagName] の値が同じ場合、すべてに同じアクションが表示されます。</span><span class="sxs-lookup"><span data-stu-id="98b89-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="98b89-112">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="98b89-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98b89-113">セル名:</span><span class="sxs-lookup"><span data-stu-id="98b89-113">Cell name:</span></span>  <br/> |<span data-ttu-id="98b89-114">アクション.</span><span class="sxs-lookup"><span data-stu-id="98b89-114">Actions.</span></span> <span data-ttu-id="98b89-115">*名前*です。tagnamewhere を指定します。</span><span class="sxs-lookup"><span data-stu-id="98b89-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="98b89-116">*name*は、Actions 行の名前です。</span><span class="sxs-lookup"><span data-stu-id="98b89-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="98b89-117">プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="98b89-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="98b89-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="98b89-118">Section index:</span></span>  <br/> |<span data-ttu-id="98b89-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="98b89-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="98b89-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="98b89-120">Row index:</span></span>  <br/> |<span data-ttu-id="98b89-121">**visRowAction** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="98b89-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="98b89-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="98b89-122">Cell index:</span></span>  <br/> |<span data-ttu-id="98b89-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="98b89-123">**visActionTagName**</span></span> <br/> |
   

