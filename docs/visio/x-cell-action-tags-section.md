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
description: アクション タグ ボタンを配置する図形のローカル座標の x 座標位置。
ms.openlocfilehash: 9f26bec81563c9813a88ed5c69730266834ee101
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431114"
---
# <a name="x-cell-action-tags-section"></a><span data-ttu-id="4f2a1-103">[X] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="4f2a1-103">X Cell (Action Tags Section)</span></span>

<span data-ttu-id="4f2a1-104">アクション  *タグ*  ボタンを配置する図形のローカル座標の x 座標位置。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-104">The  *x*  -coordinate position in the shape's local coordinates around which the action tag button is placed.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="4f2a1-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4f2a1-106">注釈</span><span class="sxs-lookup"><span data-stu-id="4f2a1-106">Remarks</span></span>

<span data-ttu-id="4f2a1-107">[X] セルと [Y] セルは、図形のローカル座標内の 1 つの点を定義し、[X Justify] セルと [Y Justify] セルは、その点からのアクション タグ ボタンの相対位置を定義します。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-107">The X and Y cells define a point in the shape's local coordinates, and the X Justify and Y Justify cells define where to place the action tag button in relation to that point.</span></span> 
  
<span data-ttu-id="4f2a1-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-108">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f2a1-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="4f2a1-109">Cell name:</span></span>  <br/> |<span data-ttu-id="4f2a1-110">SmartTags。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-110">SmartTags.</span></span> <span data-ttu-id="4f2a1-111">*name*  .X は SmartTags です。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-111">*name*  .X           where SmartTags.</span></span> <span data-ttu-id="4f2a1-112">*name*  はアクション タグ行の名前です。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-112">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="4f2a1-113">プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="4f2a1-113">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4f2a1-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="4f2a1-114">Section index:</span></span>  <br/> |<span data-ttu-id="4f2a1-115">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="4f2a1-115">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="4f2a1-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="4f2a1-116">Row index:</span></span>  <br/> |<span data-ttu-id="4f2a1-117">**visRowSmartTag**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="4f2a1-117">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="4f2a1-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="4f2a1-118">Cell index:</span></span>  <br/> |<span data-ttu-id="4f2a1-119">**visSmartTagX**</span><span class="sxs-lookup"><span data-stu-id="4f2a1-119">**visSmartTagX**</span></span> <br/> |
   

