---
title: '[X] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60093
localization_priority: Normal
ms.assetid: d13e362b-9b69-30c5-003a-9c5df2aa29f6
description: X 座標の位置に図形のローカル座標の中心となる操作タグ ボタンが配置されます。
ms.openlocfilehash: f6b3a57b825c96398058e7b71e3cebeb8480dd49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806801"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="6100c-103">[X] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="6100c-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="6100c-104">*X* -図形のローカル座標の内、操作タグ ボタンが配置される位置を調整します。</span><span class="sxs-lookup"><span data-stu-id="6100c-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6100c-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="6100c-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6100c-106">備考</span><span class="sxs-lookup"><span data-stu-id="6100c-106">Remarks</span></span>

<span data-ttu-id="6100c-107">[X] セルと [Y] セルは、図形のローカル座標内の 1 つの点を定義し、[X Justify] セルと [Y Justify] セルは、その点からのアクション タグ ボタンの相対位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="6100c-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="6100c-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="6100c-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6100c-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="6100c-109">Cell name:</span></span>  <br/> |<span data-ttu-id="6100c-110">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="6100c-110">SmartTags.</span></span> <span data-ttu-id="6100c-111">*名*です。X スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="6100c-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="6100c-112">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="6100c-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="6100c-113">プログラムから、インデックスによって [X] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="6100c-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6100c-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="6100c-114">Section index:</span></span>  <br/> |<span data-ttu-id="6100c-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="6100c-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="6100c-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="6100c-116">Row index:</span></span>  <br/> |<span data-ttu-id="6100c-117">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="6100c-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6100c-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="6100c-118">Cell index:</span></span>  <br/> |<span data-ttu-id="6100c-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="6100c-119">**visSmartTagX**</span></span> <br/> |
   

