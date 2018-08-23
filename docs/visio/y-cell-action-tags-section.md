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
description: Y-図形のローカル座標の内、操作タグ ボタンが配置される位置を調整します。
ms.openlocfilehash: 641c868703c6e4b0b7e749f68813b5869b5728c0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806831"
---
# <a name="y-cell-action-tags-section"></a><span data-ttu-id="df73f-103">[Y] セル ([操作タグ] セクション)</span><span class="sxs-lookup"><span data-stu-id="df73f-103">Y Cell (Action Tags Section)</span></span>

<span data-ttu-id="df73f-104">*Y* -図形のローカル座標の内、操作タグ ボタンが配置される位置を調整します。</span><span class="sxs-lookup"><span data-stu-id="df73f-104">The  *y*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="df73f-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="df73f-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="df73f-106">備考</span><span class="sxs-lookup"><span data-stu-id="df73f-106">Remarks</span></span>

<span data-ttu-id="df73f-107">[X] セルと [Y] セルは、図形のローカル座標内の 1 つの点を定義し、[X Justify] セルと [Y Justify] セルは、その点からのアクション タグ ボタンの相対位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="df73f-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="df73f-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="df73f-108">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df73f-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="df73f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="df73f-110">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="df73f-110">SmartTags.</span></span>  <span data-ttu-id="df73f-111">*名*です。Y、スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="df73f-111">*name*  .Y           where SmartTags.</span></span> <span data-ttu-id="df73f-112">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="df73f-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="df73f-113">プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="df73f-113">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df73f-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="df73f-114">Section index:</span></span>  <br/> |<span data-ttu-id="df73f-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="df73f-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="df73f-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="df73f-116">Row index:</span></span>  <br/> |<span data-ttu-id="df73f-117">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="df73f-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="df73f-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="df73f-118">Cell index:</span></span>  <br/> |<span data-ttu-id="df73f-119">**visSmartTagY**</span><span class="sxs-lookup"><span data-stu-id="df73f-119">**visSmartTagY**</span></span> <br/> |
   

