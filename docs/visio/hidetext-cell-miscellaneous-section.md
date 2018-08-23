---
title: '[HideText] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251323
localization_priority: Normal
ms.assetid: 3d23647a-e567-da71-50df-336a0f2f4071
description: 図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。
ms.openlocfilehash: e2d220e9d7874382f2aaeade5488bd4809f3a9dd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805536"
---
# <a name="hidetext-cell-miscellaneous-section"></a><span data-ttu-id="af82e-104">[HideText] セル ([その他] セクション)</span><span class="sxs-lookup"><span data-stu-id="af82e-104">HideText Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="af82e-p102">図形のテキストを非表示にします。テキストを非表示にしても、テキスト ブロック内のテキストの参照、プロパティの編集、およびスタイルの適用は可能ですが、[HideText] の値を FALSE (0) に戻すまで、変更内容は表示されません。</span><span class="sxs-lookup"><span data-stu-id="af82e-p102">Hides the text for a shape. You can view text, edit properties, and apply styles to the text in the text block, although the changes will not appear until you reset HideText to FALSE (0).</span></span>
  
|<span data-ttu-id="af82e-107">**値**</span><span class="sxs-lookup"><span data-stu-id="af82e-107">**Value**</span></span>|<span data-ttu-id="af82e-108">**説明**</span><span class="sxs-lookup"><span data-stu-id="af82e-108">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="af82e-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="af82e-109">TRUE</span></span>  <br/> | <span data-ttu-id="af82e-110">テキストは表示されず、印刷もされません。</span><span class="sxs-lookup"><span data-stu-id="af82e-110">Text is hidden and does not print.</span></span>  <br/> |
| <span data-ttu-id="af82e-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="af82e-111">FALSE</span></span>  <br/> | <span data-ttu-id="af82e-112">テキストは表示されます。</span><span class="sxs-lookup"><span data-stu-id="af82e-112">Text is not hidden.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af82e-113">備考</span><span class="sxs-lookup"><span data-stu-id="af82e-113">Remarks</span></span>

<span data-ttu-id="af82e-114">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[HideText] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="af82e-114">To get a reference to the HideText cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af82e-115">セル名:</span><span class="sxs-lookup"><span data-stu-id="af82e-115">Cell name:</span></span>  <br/> | <span data-ttu-id="af82e-116">HideText</span><span class="sxs-lookup"><span data-stu-id="af82e-116">HideText</span></span>  <br/> |
   
<span data-ttu-id="af82e-117">プログラムから、インデックスによって [HideText] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="af82e-117">To get a reference to the HideText cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="af82e-118">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="af82e-118">Section index:</span></span>  <br/> |<span data-ttu-id="af82e-119">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="af82e-119">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="af82e-120">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="af82e-120">Row index:</span></span>  <br/> |<span data-ttu-id="af82e-121">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="af82e-121">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="af82e-122">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="af82e-122">Cell index:</span></span>  <br/> |<span data-ttu-id="af82e-123">**visHideText**</span><span class="sxs-lookup"><span data-stu-id="af82e-123">**visHideText**</span></span> <br/> |
   

