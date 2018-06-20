---
title: '[Size] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251252
localization_priority: Normal
ms.assetid: a61b50fe-eacb-b3d4-0e4e-ab3e7c972ee9
description: 図形のテキスト ブロックにあるテキストのサイズを指定します。
ms.openlocfilehash: f3077441844b859cf224eccc8180d0d56cce851f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806497"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="812e7-103">[Size] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="812e7-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="812e7-104">図形のテキスト ブロックにあるテキストのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="812e7-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="812e7-105">備考</span><span class="sxs-lookup"><span data-stu-id="812e7-105">Remarks</span></span>

<span data-ttu-id="812e7-p101">テキストのサイズは図面の縮尺による影響を受けません。図面の縮尺を変更しても、テキストのサイズは変わりません。</span><span class="sxs-lookup"><span data-stu-id="812e7-p101">The text's size is independent of the scale of the drawing. If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="812e7-108">別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Size] セルへの参照を取得、次のように使用します。</span><span class="sxs-lookup"><span data-stu-id="812e7-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="812e7-109">セル名:</span><span class="sxs-lookup"><span data-stu-id="812e7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="812e7-110">Char.Size [ *i* ]、 *i* = < 1 > では、2、3.</span><span class="sxs-lookup"><span data-stu-id="812e7-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="812e7-111">プログラムから、インデックスによって [Size] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。</span><span class="sxs-lookup"><span data-stu-id="812e7-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="812e7-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="812e7-112">Section index:</span></span>  <br/> |<span data-ttu-id="812e7-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="812e7-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="812e7-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="812e7-114">Row index:</span></span>  <br/> |<span data-ttu-id="812e7-115">**visRowCharacter** +  *i* 、 *i* = 0, 1, 2.</span><span class="sxs-lookup"><span data-stu-id="812e7-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="812e7-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="812e7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="812e7-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="812e7-117">**visCharacterSize**</span></span> <br/> |
   

