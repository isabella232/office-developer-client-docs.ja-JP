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
description: 図形のローカル座標で、アクションタグボタンが配置される位置の x 座標です。
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335778"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="a3a0a-103">[X] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="a3a0a-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="a3a0a-104">図形のローカル座標で、アクションタグボタンが配置される位置の*x*座標です。</span><span class="sxs-lookup"><span data-stu-id="a3a0a-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a3a0a-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="a3a0a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a3a0a-106">解説</span><span class="sxs-lookup"><span data-stu-id="a3a0a-106">Remarks</span></span>

<span data-ttu-id="a3a0a-107">[X] セルと [Y] セルは、図形のローカル座標内の 1 つの点を定義し、[X Justify] セルと [Y Justify] セルは、その点からのアクション タグ ボタンの相対位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="a3a0a-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="a3a0a-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="a3a0a-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3a0a-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="a3a0a-109">Cell name:</span></span>  <br/> |<span data-ttu-id="a3a0a-110">タグ.</span><span class="sxs-lookup"><span data-stu-id="a3a0a-110">SmartTags.</span></span> <span data-ttu-id="a3a0a-111">*名前*です。X にスマートタグを指定します。</span><span class="sxs-lookup"><span data-stu-id="a3a0a-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="a3a0a-112">*name*は、アクションタグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="a3a0a-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="a3a0a-113">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="a3a0a-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="a3a0a-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="a3a0a-114">Section index:</span></span>  <br/> |<span data-ttu-id="a3a0a-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="a3a0a-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="a3a0a-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="a3a0a-116">Row index:</span></span>  <br/> |<span data-ttu-id="a3a0a-117">**visRowSmartTag** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="a3a0a-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="a3a0a-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="a3a0a-118">Cell index:</span></span>  <br/> |<span data-ttu-id="a3a0a-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="a3a0a-119">**visSmartTagX**</span></span> <br/> |
   

