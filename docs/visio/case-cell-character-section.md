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
ms.openlocfilehash: 50ceaa1188caded40d36b8837c346fbbba2e14d2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434348"
---
# <a name="case-cell-character-section"></a><span data-ttu-id="0cc59-105">[Case] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="0cc59-105">Case Cell (Character Section)</span></span>

<span data-ttu-id="0cc59-p102">図形のテキストでの大文字小文字による区別を指定します。すべて大文字 (1) および先頭文字のみ大文字 (2) を選択した場合、すべてのテキストを大文字で入力すると、テキストの表示状態は変わりません。この 2 つのオプションを有効にするには、テキストを小文字で入力する必要があります。</span><span class="sxs-lookup"><span data-stu-id="0cc59-p102">Determines the case of a shape's text. All capital (uppercase) letters (1) and initial capital letters (2) do not change the appearance of text that was entered in all capital letters. The text must be entered in lowercase letters for these options to show an effect.</span></span>
  
|<span data-ttu-id="0cc59-109">**値**</span><span class="sxs-lookup"><span data-stu-id="0cc59-109">**Value**</span></span>|<span data-ttu-id="0cc59-110">**説明**</span><span class="sxs-lookup"><span data-stu-id="0cc59-110">**Description**</span></span>|<span data-ttu-id="0cc59-111">**オートメーション定数**</span><span class="sxs-lookup"><span data-stu-id="0cc59-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="0cc59-112">0</span><span class="sxs-lookup"><span data-stu-id="0cc59-112">0</span></span>  <br/> | <span data-ttu-id="0cc59-113">通常</span><span class="sxs-lookup"><span data-stu-id="0cc59-113">Normal case</span></span>  <br/> |<span data-ttu-id="0cc59-114">**visCaseNormal**</span><span class="sxs-lookup"><span data-stu-id="0cc59-114">**visCaseNormal**</span></span> <br/> |
| <span data-ttu-id="0cc59-115">1</span><span class="sxs-lookup"><span data-stu-id="0cc59-115">1</span></span>  <br/> | <span data-ttu-id="0cc59-116">すべて大文字</span><span class="sxs-lookup"><span data-stu-id="0cc59-116">All capital (uppercase) letters</span></span>  <br/> |<span data-ttu-id="0cc59-117">**visCaseAllCaps**</span><span class="sxs-lookup"><span data-stu-id="0cc59-117">**visCaseAllCaps**</span></span> <br/> |
| <span data-ttu-id="0cc59-118">2</span><span class="sxs-lookup"><span data-stu-id="0cc59-118">2</span></span>  <br/> | <span data-ttu-id="0cc59-119">先頭文字のみ大文字</span><span class="sxs-lookup"><span data-stu-id="0cc59-119">Initial capital letters only</span></span>  <br/> |<span data-ttu-id="0cc59-120">**visCaseInitialCaps**</span><span class="sxs-lookup"><span data-stu-id="0cc59-120">**visCaseInitialCaps**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0cc59-121">注釈</span><span class="sxs-lookup"><span data-stu-id="0cc59-121">Remarks</span></span>

<span data-ttu-id="0cc59-122">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Case] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="0cc59-122">To get a reference to the Case cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cc59-123">セル名 :</span><span class="sxs-lookup"><span data-stu-id="0cc59-123">Cell name:</span></span>  <br/> | <span data-ttu-id="0cc59-124">Char.Case[  *i*  ] ここで  *、i*  = <1>、2、3、..</span><span class="sxs-lookup"><span data-stu-id="0cc59-124">Char.Case[  *i*  ]            where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="0cc59-125">プログラムから、インデックスによって [Case] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="0cc59-125">To get a reference to the Case cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0cc59-126">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="0cc59-126">Section index:</span></span>  <br/> |<span data-ttu-id="0cc59-127">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="0cc59-127">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="0cc59-128">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="0cc59-128">Row index:</span></span>  <br/> |<span data-ttu-id="0cc59-129">**visRowCharacter**  +  *i* *=* 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="0cc59-129">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
| <span data-ttu-id="0cc59-130">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="0cc59-130">Cell index:</span></span>  <br/> |<span data-ttu-id="0cc59-131">**visCharacterCase**</span><span class="sxs-lookup"><span data-stu-id="0cc59-131">**visCharacterCase**</span></span> <br/> |
   

