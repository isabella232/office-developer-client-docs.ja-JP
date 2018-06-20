---
title: '[X Justify] セル ([Action Tags] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1026936
localization_priority: Normal
ms.assetid: a8995020-3eaa-2b2c-eca0-dd475de4d06f
description: X、X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。
ms.openlocfilehash: 043d7b198ae5a529c623545fb54ef5aa1d32217d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806812"
---
# <a name="x-justify-cell-action-tags-section"></a><span data-ttu-id="bd3f7-103">[X Justify] セル ([Action Tags] セクション)</span><span class="sxs-lookup"><span data-stu-id="bd3f7-103">X Justify Cell (Action Tags Section)</span></span>

<span data-ttu-id="bd3f7-104">*X*の X と Y セルによって定義された点を基準にして、操作タグ ボタンのオフセット。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-104">The  *x*  -offset of the action tag button relative to the point defined by the X and Y cells.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bd3f7-105">Microsoft Visio の以前のバージョンでは、アクション タグは、スマート タグと呼ばれていました。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="bd3f7-106">**値**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-106">**Value**</span></span>|<span data-ttu-id="bd3f7-107">**説明**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-107">**Description**</span></span>|<span data-ttu-id="bd3f7-108">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="bd3f7-109">0</span><span class="sxs-lookup"><span data-stu-id="bd3f7-109">0</span></span>  <br/> | <span data-ttu-id="bd3f7-110">左揃えします (既定値)。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-110">Left justified (the default).</span></span>  <br/> |<span data-ttu-id="bd3f7-111">**visSmartTagXJustifyLeft**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-111">**visSmartTagXJustifyLeft**</span></span> <br/> |
| <span data-ttu-id="bd3f7-112">1</span><span class="sxs-lookup"><span data-stu-id="bd3f7-112">1</span></span>  <br/> | <span data-ttu-id="bd3f7-113">中央揃え</span><span class="sxs-lookup"><span data-stu-id="bd3f7-113">Centered.</span></span>  <br/> |<span data-ttu-id="bd3f7-114">**visSmartTagXJustifyCenter**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-114">**visSmartTagXJustifyCenter**</span></span> <br/> |
| <span data-ttu-id="bd3f7-115">2</span><span class="sxs-lookup"><span data-stu-id="bd3f7-115">2</span></span>  <br/> | <span data-ttu-id="bd3f7-116">右揃えします。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-116">Right justified.</span></span>  <br/> |<span data-ttu-id="bd3f7-117">**visSmartTagXJustifyRight**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-117">**visSmartTagXJustifyRight**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd3f7-118">備考</span><span class="sxs-lookup"><span data-stu-id="bd3f7-118">Remarks</span></span>

<span data-ttu-id="bd3f7-119">X Justify] および [Y Justify] の各セルは、X と Y のセルで定義されているポイントを基準にして、操作タグ ボタンを配置する場所を決定します。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-119">The X Justify and Y Justify cells determine where the action tag button is placed in relation to the point defined in the X and Y cells.</span></span> 
  
<span data-ttu-id="bd3f7-120">取得する、[X Justify] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-120">To get a reference to the X Justify cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd3f7-121">セル名:</span><span class="sxs-lookup"><span data-stu-id="bd3f7-121">Cell name:</span></span>  <br/> | <span data-ttu-id="bd3f7-122">スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-122">SmartTags.</span></span>  <span data-ttu-id="bd3f7-123">*名*です。XJustify、スマート タグです。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-123">*name*  .XJustify           where SmartTags.</span></span> <span data-ttu-id="bd3f7-124">*タグのアクション行の名前します。*</span><span class="sxs-lookup"><span data-stu-id="bd3f7-124">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="bd3f7-125">プログラムから、インデックスによって [X Justify] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="bd3f7-125">To get a reference to the X Justify cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd3f7-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd3f7-126">Section index:</span></span>  <br/> |<span data-ttu-id="bd3f7-127">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-127">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="bd3f7-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd3f7-128">Row index:</span></span>  <br/> |<span data-ttu-id="bd3f7-129">**visRowSmartTag** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="bd3f7-129">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="bd3f7-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="bd3f7-130">Cell index:</span></span>  <br/> |<span data-ttu-id="bd3f7-131">**visSmartTagXJustify**</span><span class="sxs-lookup"><span data-stu-id="bd3f7-131">**visSmartTagXJustify**</span></span> <br/> |
   

