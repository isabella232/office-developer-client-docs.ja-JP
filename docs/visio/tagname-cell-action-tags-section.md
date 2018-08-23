---
title: '[TagName] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60088
localization_priority: Normal
ms.assetid: 28d1cd60-4fb6-9feb-1a13-0962798ac1ad
description: アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。
ms.openlocfilehash: dbac3d4dff9d2ffd18bba75db56cafc08f5e0ee8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806603"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="f632b-103">[TagName] セル ([操作タグ] セクション)</span><span class="sxs-lookup"><span data-stu-id="f632b-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="f632b-104">アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。</span><span class="sxs-lookup"><span data-stu-id="f632b-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f632b-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="f632b-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f632b-106">備考</span><span class="sxs-lookup"><span data-stu-id="f632b-106">Remarks</span></span>

 <span data-ttu-id="f632b-107">操作タグ セクションの [tagname] セルとそのアクションのアクション タグを関連付けるには [操作] セクションの [tagname] セルと一緒に動作します。</span><span class="sxs-lookup"><span data-stu-id="f632b-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="f632b-108">[操作] セクション内の行も [tagname] セルがあり、このセルと同じ [tagname] セルの値がある行がこのアクションのタグに対して実行するアクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="f632b-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="f632b-109">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f632b-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f632b-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="f632b-110">Cell name:</span></span>  <br/> | <span data-ttu-id="f632b-111">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="f632b-111">SmartTags.</span></span>  <span data-ttu-id="f632b-112">*名*です。タグ名、スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="f632b-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="f632b-113">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="f632b-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="f632b-114">プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f632b-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f632b-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f632b-115">Section index:</span></span>  <br/> |<span data-ttu-id="f632b-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="f632b-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="f632b-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f632b-117">Row index:</span></span>  <br/> |<span data-ttu-id="f632b-118">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="f632b-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f632b-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f632b-119">Cell index:</span></span>  <br/> |<span data-ttu-id="f632b-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="f632b-120">**visSmartTagName**</span></span> <br/> |
   

