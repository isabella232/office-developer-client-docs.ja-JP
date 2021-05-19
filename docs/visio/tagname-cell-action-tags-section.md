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
ms.openlocfilehash: 777d6c1098888c9835c1ad367bb70926b835180b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417911"
---
# <a name="tagname-cell-action-tags-section"></a><span data-ttu-id="16c43-103">[TagName] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="16c43-103">TagName Cell (Action Tags Section)</span></span>

<span data-ttu-id="16c43-104">アクション タグとそのアクションを関連付けるキーとして使用されるアクション タグの名前です。</span><span class="sxs-lookup"><span data-stu-id="16c43-104">Name of the action tag that is used as a key to associate the action tag with its actions.</span></span>
  
> [!NOTE]
> <span data-ttu-id="16c43-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="16c43-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="16c43-106">注釈</span><span class="sxs-lookup"><span data-stu-id="16c43-106">Remarks</span></span>

 <span data-ttu-id="16c43-107">[Action Tags] セクションの [TagName] セルは、[Actions] セクションの [TagName] セルと一緒に、アクション タグとそのアクションを関連付ける働きをします。</span><span class="sxs-lookup"><span data-stu-id="16c43-107">The TagName cell in the Action Tags section works together with the TagName cell in the Actions section to associate an action tag with its actions.</span></span> <span data-ttu-id="16c43-108">[アクション] セクションの行には [TagName] セルも含まれます。また、このセルと同じ TagName セル値を持つ行は、このアクション タグに対して実行するアクションを定義します。</span><span class="sxs-lookup"><span data-stu-id="16c43-108">Rows in the Actions section also have a TagName cell, and those rows with the same TagName cell value as this cell define actions to take for this action tag.</span></span> 
  
<span data-ttu-id="16c43-109">別の数式から、または **CellsU** プロパティを使用してプログラムから、名前によって [TagName] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="16c43-109">To get a reference to the TagName cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16c43-110">セル名:</span><span class="sxs-lookup"><span data-stu-id="16c43-110">Cell name:</span></span>  <br/> | <span data-ttu-id="16c43-111">SmartTags。</span><span class="sxs-lookup"><span data-stu-id="16c43-111">SmartTags.</span></span>  <span data-ttu-id="16c43-112">*name*  .SmartTags の TagName。</span><span class="sxs-lookup"><span data-stu-id="16c43-112">*name*  .TagName           where SmartTags.</span></span> <span data-ttu-id="16c43-113">*name*  はアクション タグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="16c43-113">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="16c43-114">プログラムから、インデックスによって [TagName] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="16c43-114">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="16c43-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="16c43-115">Section index:</span></span>  <br/> |<span data-ttu-id="16c43-116">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="16c43-116">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="16c43-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="16c43-117">Row index:</span></span>  <br/> |<span data-ttu-id="16c43-118">**visRowSmartTag**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="16c43-118">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="16c43-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="16c43-119">Cell index:</span></span>  <br/> |<span data-ttu-id="16c43-120">**visSmartTagName**</span><span class="sxs-lookup"><span data-stu-id="16c43-120">**visSmartTagName**</span></span> <br/> |
   

