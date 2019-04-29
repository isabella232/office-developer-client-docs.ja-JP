---
title: '[Y] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026934
localization_priority: Normal
ms.assetid: b213fc46-7f80-99fd-60ba-8ddf3d0f6ee3
description: 図形のローカル座標で、アクションタグボタンが配置される位置の y 座標です。
ms.openlocfilehash: 02797a849a262cb506f4617aadaccedabccdab77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430225"
---
# <a name="y-cell-action-tags-section"></a><span data-ttu-id="23c11-103">[Y] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="23c11-103">Y Cell (Action Tags Section)</span></span>

<span data-ttu-id="23c11-104">図形のローカル座標で、アクションタグボタンが配置される位置の*y*座標です。</span><span class="sxs-lookup"><span data-stu-id="23c11-104">The  *y*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="23c11-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="23c11-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="23c11-106">注釈</span><span class="sxs-lookup"><span data-stu-id="23c11-106">Remarks</span></span>

<span data-ttu-id="23c11-107">[X] セルと [Y] セルは、図形のローカル座標内の 1 つの点を定義し、[X Justify] セルと [Y Justify] セルは、その点からのアクション タグ ボタンの相対位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="23c11-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="23c11-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="23c11-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23c11-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="23c11-109">Cell name:</span></span>  <br/> | <span data-ttu-id="23c11-110">タグ.</span><span class="sxs-lookup"><span data-stu-id="23c11-110">SmartTags.</span></span>  <span data-ttu-id="23c11-111">*名前*です。Y のスマート位置。</span><span class="sxs-lookup"><span data-stu-id="23c11-111">*name*  .Y           where SmartTags.</span></span> <span data-ttu-id="23c11-112">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="23c11-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="23c11-113">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="23c11-113">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="23c11-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="23c11-114">Section index:</span></span>  <br/> |<span data-ttu-id="23c11-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="23c11-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="23c11-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="23c11-116">Row index:</span></span>  <br/> |<span data-ttu-id="23c11-117">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="23c11-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="23c11-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="23c11-118">Cell index:</span></span>  <br/> |<span data-ttu-id="23c11-119">**visSmartTagY**</span><span class="sxs-lookup"><span data-stu-id="23c11-119">**visSmartTagY**</span></span> <br/> |
   

