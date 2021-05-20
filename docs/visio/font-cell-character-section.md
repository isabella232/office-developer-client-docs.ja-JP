---
title: '[Font] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm390
localization_priority: Normal
ms.assetid: 935760a9-307e-90bc-c301-d04283d97427
description: テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。
ms.openlocfilehash: d9182932b8fa63c30473b93e420aa9efe30bf5eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438667"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="e3c61-105">[Font] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="e3c61-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="e3c61-p102">テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。</span><span class="sxs-lookup"><span data-stu-id="e3c61-p102">Represents the number of the font used to format the text. Font numbers vary according to the fonts installed on your system. The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e3c61-109">注釈</span><span class="sxs-lookup"><span data-stu-id="e3c61-109">Remarks</span></span>

<span data-ttu-id="e3c61-110">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Font] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="e3c61-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3c61-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="e3c61-111">Cell name:</span></span>  <br/> | <span data-ttu-id="e3c61-112">Char.Font[  *i*  ] ここで  *、i*  = <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="e3c61-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="e3c61-113">プログラムから、インデックスによって [Font] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="e3c61-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e3c61-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="e3c61-114">Section index:</span></span>  <br/> |<span data-ttu-id="e3c61-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="e3c61-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="e3c61-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="e3c61-116">Row index:</span></span>  <br/> |<span data-ttu-id="e3c61-117">**visRowCharacter**  +  *i* *=* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e3c61-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="e3c61-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="e3c61-118">Cell index:</span></span>  <br/> |<span data-ttu-id="e3c61-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="e3c61-119">**visCharacterFont**</span></span> <br/> |
   

