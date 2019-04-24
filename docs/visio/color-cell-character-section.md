---
title: '[Color] セル ([Character] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm160
localization_priority: Normal
ms.assetid: 1c9aab2e-6c2f-0684-4e66-c35ac71883d6
description: 図形のテキストに使用する色を指定します。
ms.openlocfilehash: a27d957781ca9a784e7ab9d5c1ce4f533b9a55ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341840"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="b7c4c-103">[Color] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="b7c4c-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="b7c4c-104">図形のテキストに使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b7c4c-105">解説</span><span class="sxs-lookup"><span data-stu-id="b7c4c-105">Remarks</span></span>

<span data-ttu-id="b7c4c-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="b7c4c-107">ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="b7c4c-108">ユーザー設定の色の値は rgb カラーで、数字ではなく rgb ( *r, g, b*) は [シェイプシート] ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="b7c4c-109">ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="b7c4c-110">テキストの色の透過性を設定するには、[Transparency] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="b7c4c-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7c4c-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="b7c4c-112">Cell name:</span></span>  <br/> |<span data-ttu-id="b7c4c-113">文字の色 [ *i* ] = \*\* <1>、2、3、...</span><span class="sxs-lookup"><span data-stu-id="b7c4c-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="b7c4c-114">プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="b7c4c-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b7c4c-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7c4c-115">Section index:</span></span>  <br/> |<span data-ttu-id="b7c4c-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="b7c4c-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="b7c4c-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7c4c-117">Row index:</span></span>  <br/> |<span data-ttu-id="b7c4c-118">**visRowCharacter** +  *i* = \*\* 0、1、2、...</span><span class="sxs-lookup"><span data-stu-id="b7c4c-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="b7c4c-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="b7c4c-119">Cell index:</span></span>  <br/> |<span data-ttu-id="b7c4c-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="b7c4c-120">**visCharacterColor**</span></span> <br/> |
   

