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
ms.openlocfilehash: cbbf2a2400c995e0cbc217c1161fbd18f7459b28
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805410"
---
# <a name="font-cell-character-section"></a><span data-ttu-id="de660-105">[Font] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="de660-105">Font Cell (Character Section)</span></span>

<span data-ttu-id="de660-p102">テキストの書式設定に使用するフォントの番号を表します。フォント番号は、システムにインストールされたフォントによって異なります。フォント番号は既定のフォントを示し、通常はＭＳ Ｐゴシックです。</span><span class="sxs-lookup"><span data-stu-id="de660-p102">Represents the number of the font used to format the text. Font numbers vary according to the fonts installed on your system. The number 0 represents the default font, which is typically Arial.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="de660-109">備考</span><span class="sxs-lookup"><span data-stu-id="de660-109">Remarks</span></span>

<span data-ttu-id="de660-110">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Font] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="de660-110">To get a reference to the Font cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de660-111">セル名:</span><span class="sxs-lookup"><span data-stu-id="de660-111">Cell name:</span></span>  <br/> | <span data-ttu-id="de660-112">Char.Font [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="de660-112">Char.Font[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="de660-113">プログラムから、インデックスによって [Font] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="de660-113">To get a reference to the Font cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="de660-114">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="de660-114">Section index:</span></span>  <br/> |<span data-ttu-id="de660-115">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="de660-115">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="de660-116">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="de660-116">Row index:</span></span>  <br/> |<span data-ttu-id="de660-117">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="de660-117">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="de660-118">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="de660-118">Cell index:</span></span>  <br/> |<span data-ttu-id="de660-119">**visCharacterFont**</span><span class="sxs-lookup"><span data-stu-id="de660-119">**visCharacterFont**</span></span> <br/> |
   

