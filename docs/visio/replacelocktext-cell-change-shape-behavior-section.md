---
title: '[ReplaceLockText] セル ([図形の動作の変更] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。 ReplaceLockText は、マスター上に表示されるテキストが置換される図形のテキストを上書きするかどうかを決定します。
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806235"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="d1adf-104">[ReplaceLockText] セル ([図形の動作の変更] セクション)</span><span class="sxs-lookup"><span data-stu-id="d1adf-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="d1adf-105">マスター シェイプ内の指定したセルの値が図形の置換操作の実行中に置換される図形の値 (ローカル値を含む) を上書きするかどうかを示します。</span><span class="sxs-lookup"><span data-stu-id="d1adf-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="d1adf-106">**ReplaceLockText**は、マスター上に表示されるテキストが置換される図形のテキストを上書きするかどうかを決定します。</span><span class="sxs-lookup"><span data-stu-id="d1adf-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="d1adf-107">**値**</span><span class="sxs-lookup"><span data-stu-id="d1adf-107">**Value**</span></span>|<span data-ttu-id="d1adf-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="d1adf-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d1adf-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="d1adf-109">TRUE</span></span>  <br/> | <span data-ttu-id="d1adf-p103">マスター シェイプのテキストは、古い図形のテキストに優先します。さらに、マスター シェイプは、図形の置換操作中、次のセクション内のセルの値に優先します。</span><span class="sxs-lookup"><span data-stu-id="d1adf-p103">The text on the master shape overwrites the text on the old shape. In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:  </span></span><br/> <span data-ttu-id="d1adf-112">**テキスト フィールド**] セクション</span><span class="sxs-lookup"><span data-stu-id="d1adf-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="d1adf-113">**テキスト ブロックの書式**セクション</span><span class="sxs-lookup"><span data-stu-id="d1adf-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="d1adf-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="d1adf-114">FALSE</span></span>  <br/> |<span data-ttu-id="d1adf-115">置換後の図形には、その図形に追加された、古い図形からのテキスト、テキスト フィールド、またはその他のテキスト プロパティが格納されます。</span><span class="sxs-lookup"><span data-stu-id="d1adf-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="d1adf-116">置換後の図形には、古い図形からテキストのプロパティが含まれている、置換後の図形も値があります、**文字**および**段落**の前のセクションから 1 つ以上の行がある場合。</span><span class="sxs-lookup"><span data-stu-id="d1adf-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="d1adf-117">TRUE (1) に設定されると、マスター シェイプの値が、置換される図形の次の値に置換されます。</span><span class="sxs-lookup"><span data-stu-id="d1adf-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- <span data-ttu-id="d1adf-118">[[TheText] セル ([Events] セクション)](thetext-cell-events-section.md)</span><span class="sxs-lookup"><span data-stu-id="d1adf-118">[TheText Cell (Events Section)](thetext-cell-events-section.md)</span></span>
    
- <span data-ttu-id="d1adf-119">[[Character] セクション](character-section.md)内のセル</span><span class="sxs-lookup"><span data-stu-id="d1adf-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="d1adf-120">[[Paragraph] セクション](paragraph-section.md)内のセル</span><span class="sxs-lookup"><span data-stu-id="d1adf-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="d1adf-121">[[Tabs] セクション](tabs-section.md)内のセル</span><span class="sxs-lookup"><span data-stu-id="d1adf-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d1adf-122">備考</span><span class="sxs-lookup"><span data-stu-id="d1adf-122">Remarks</span></span>

<span data-ttu-id="d1adf-123">**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ReplaceLockText** ] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="d1adf-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1adf-124">セル名:</span><span class="sxs-lookup"><span data-stu-id="d1adf-124">Cell name:</span></span>  <br/> | <span data-ttu-id="d1adf-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="d1adf-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="d1adf-126">プログラムから、インデックスによって [ **ReplaceLockText** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1adf-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d1adf-127">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1adf-127">Section index:</span></span>  <br/> |<span data-ttu-id="d1adf-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d1adf-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d1adf-129">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1adf-129">Row index:</span></span>  <br/> |<span data-ttu-id="d1adf-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="d1adf-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="d1adf-131">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1adf-131">Cell index:</span></span>  <br/> |<span data-ttu-id="d1adf-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="d1adf-132">**visReplaceLockText**</span></span> <br/> |
   

