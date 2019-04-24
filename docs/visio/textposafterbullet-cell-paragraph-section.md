---
title: '[TextPosAfterBullet] セル ([Paragraph] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60089
localization_priority: Normal
ms.assetid: 08958abb-9d66-5a83-dac3-4cbfd1f6d85e
description: 段落の第 1 行目と箇条書き行頭文字の間の距離を表します。
ms.openlocfilehash: a98967cb5f9541434745c3b3d6afafde0878074a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332287"
---
# <a name="textposafterbullet-cell-paragraph-section"></a><span data-ttu-id="f4cac-103">[TextPosAfterBullet] セル ([Paragraph] セクション)</span><span class="sxs-lookup"><span data-stu-id="f4cac-103">TextPosAfterBullet Cell (Paragraph Section)</span></span>

<span data-ttu-id="f4cac-104">段落の第 1 行目と箇条書き行頭文字の間の距離を表します。</span><span class="sxs-lookup"><span data-stu-id="f4cac-104">Represents the distance between the first line of the paragraph and the bullet.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f4cac-105">解説</span><span class="sxs-lookup"><span data-stu-id="f4cac-105">Remarks</span></span>

<span data-ttu-id="f4cac-p101">この距離は、[IndFirst] セル内に含まれている距離 (既定の左インデント) に追加されます。この値は、図面の縮尺による影響を受けません。</span><span class="sxs-lookup"><span data-stu-id="f4cac-p101">This distance is added to the distance contained in the IndFirst cell, which is the default left indent. This value is independent of the scale of the drawing.</span></span> 
  
<span data-ttu-id="f4cac-108">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextPosAfterBullet] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="f4cac-108">To get a reference to the TextPosAfterBullet cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4cac-109">セル名 :</span><span class="sxs-lookup"><span data-stu-id="f4cac-109">Cell name:</span></span>  <br/> | <span data-ttu-id="f4cac-110">段落の行頭文字 [ *i* ] = <1>、 \*\* 2、3...</span><span class="sxs-lookup"><span data-stu-id="f4cac-110">Para.TextPosAfterBullet[  *i*  ]            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="f4cac-111">プログラムから、インデックスによって [TextPosAfterBullet] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="f4cac-111">To get a reference to the TextPosAfterBullet cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f4cac-112">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4cac-112">Section index:</span></span>  <br/> |<span data-ttu-id="f4cac-113">**visSectionParagraph**</span><span class="sxs-lookup"><span data-stu-id="f4cac-113">**visSectionParagraph**</span></span> <br/> |
| <span data-ttu-id="f4cac-114">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4cac-114">Row index:</span></span>  <br/> |<span data-ttu-id="f4cac-115">**visRowParagraph** +  *i* = \*\* 0、1、2...</span><span class="sxs-lookup"><span data-stu-id="f4cac-115">**visRowParagraph** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f4cac-116">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="f4cac-116">Cell index:</span></span>  <br/> |<span data-ttu-id="f4cac-117">**visTextPosAfterBullet**</span><span class="sxs-lookup"><span data-stu-id="f4cac-117">**visTextPosAfterBullet**</span></span> <br/> |
   

