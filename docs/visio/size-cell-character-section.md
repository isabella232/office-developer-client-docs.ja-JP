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
ms.openlocfilehash: ea747620301a07cafaf179106b54510edb95f7ed
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415601"
---
# <a name="size-cell-character-section"></a><span data-ttu-id="7522f-103">[Size] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="7522f-103">Size Cell (Character Section)</span></span>

<span data-ttu-id="7522f-104">図形のテキスト ブロックにあるテキストのサイズを指定します。</span><span class="sxs-lookup"><span data-stu-id="7522f-104">Determines the size of the text in the shape's text block.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7522f-105">注釈</span><span class="sxs-lookup"><span data-stu-id="7522f-105">Remarks</span></span>

<span data-ttu-id="7522f-p101">テキストのサイズは図面の縮尺による影響を受けません。図面の縮尺を変更しても、テキストのサイズは変わりません。</span><span class="sxs-lookup"><span data-stu-id="7522f-p101">The text's size is independent of the scale of the drawing. If the drawing is scaled, the text size remains the same.</span></span>
  
<span data-ttu-id="7522f-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Size] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="7522f-108">To get a reference to the Size cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7522f-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="7522f-109">Cell name:</span></span>  <br/> | <span data-ttu-id="7522f-110">Char. Size [ *i* ] = \*\* <1>、2、3...</span><span class="sxs-lookup"><span data-stu-id="7522f-110">Char.Size[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="7522f-111">プログラムから、インデックスによって [Size] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="7522f-111">To get a reference to the Size cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="7522f-112">セクション インデックス :</span><span class="sxs-lookup"><span data-stu-id="7522f-112">Section index:</span></span>  <br/> |<span data-ttu-id="7522f-113">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="7522f-113">**visSectionCharacter**</span></span> <br/> |
| <span data-ttu-id="7522f-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="7522f-114">Row index:</span></span>  <br/> |<span data-ttu-id="7522f-115">**visRowCharacter** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="7522f-115">**visRowCharacter** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="7522f-116">セル インデックス :</span><span class="sxs-lookup"><span data-stu-id="7522f-116">Cell index:</span></span>  <br/> |<span data-ttu-id="7522f-117">**visCharacterSize**</span><span class="sxs-lookup"><span data-stu-id="7522f-117">**visCharacterSize**</span></span> <br/> |
   

