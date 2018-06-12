---
title: '[Case] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251250
localization_priority: Normal
ms.assetid: cf063c05-5789-e037-700b-1e70df00e254
description: 図形のテキストでの大文字小文字による区別を指定します。すべて大文字 (1) および先頭文字のみ大文字 (2) を選択した場合、すべてのテキストを大文字で入力すると、テキストの表示状態は変わりません。この 2 つのオプションを有効にするには、テキストを小文字で入力する必要があります。
ms.openlocfilehash: 9acd786b6fa38aec42990f1fd942174367f1135e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804947"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="7a2a2-105">[Case] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="7a2a2-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="7a2a2-p102">図形のテキストでの大文字小文字による区別を指定します。すべて大文字 (1) および先頭文字のみ大文字 (2) を選択した場合、すべてのテキストを大文字で入力すると、テキストの表示状態は変わりません。この 2 つのオプションを有効にするには、テキストを小文字で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="7a2a2-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="7a2a2-109">**値**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-109">**Value**</span></span>|<span data-ttu-id="7a2a2-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-110">**Description**</span></span>|<span data-ttu-id="7a2a2-111">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="7a2a2-112">0</span><span class="sxs-lookup"><span data-stu-id="7a2a2-112">0</span></span>  <br/> | <span data-ttu-id="7a2a2-113">通常</span><span class="sxs-lookup"><span data-stu-id="7a2a2-113">Normal case</span></span>  <br/> |<span data-ttu-id="7a2a2-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="7a2a2-115">1</span><span class="sxs-lookup"><span data-stu-id="7a2a2-115">1</span></span>  <br/> | <span data-ttu-id="7a2a2-116">すべて大文字</span><span class="sxs-lookup"><span data-stu-id="7a2a2-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="7a2a2-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="7a2a2-118">2</span><span class="sxs-lookup"><span data-stu-id="7a2a2-118">2</span></span>  <br/> | <span data-ttu-id="7a2a2-119">先頭文字のみ大文字</span><span class="sxs-lookup"><span data-stu-id="7a2a2-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="7a2a2-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7a2a2-121">Remarks</span><span class="sxs-lookup"><span data-stu-id="7a2a2-121">Remarks</span></span>

<span data-ttu-id="7a2a2-122">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって Case] セルへの参照を取得するには、次のコマンドを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a2a2-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a2a2-123">セル名:</span><span class="sxs-lookup"><span data-stu-id="7a2a2-123">Cell name:</span></span>  <br/> | <span data-ttu-id="7a2a2-124">Char.Case [ *i* ]、 *i* = < 1 > では、2、3、.</span><span class="sxs-lookup"><span data-stu-id="7a2a2-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="7a2a2-125">プログラムから、インデックスによって [Case] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="7a2a2-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7a2a2-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="7a2a2-126">Section index:</span></span>  <br/> |<span data-ttu-id="7a2a2-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="7a2a2-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7a2a2-128">Row index:</span></span>  <br/> |<span data-ttu-id="7a2a2-129">**visRowCharacter** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="7a2a2-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="7a2a2-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="7a2a2-130">Cell index:</span></span>  <br/> |<span data-ttu-id="7a2a2-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="7a2a2-131">**visCharacterCase**</span></span> <br/> |
   

