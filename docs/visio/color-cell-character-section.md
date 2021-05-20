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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439990"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="2c2b7-103">[Color] セル ([Character] セクション)</span><span class="sxs-lookup"><span data-stu-id="2c2b7-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="2c2b7-104">図形のテキストに使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2c2b7-105">注釈</span><span class="sxs-lookup"><span data-stu-id="2c2b7-105">Remarks</span></span>

<span data-ttu-id="2c2b7-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="2c2b7-107">ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="2c2b7-108">カスタム色の値は RGB 色で、数値ではなく RGB( *r, g, b*) が ShapeSheet ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="2c2b7-109">ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="2c2b7-110">テキストの色の透過性を設定するには、[Transparency] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="2c2b7-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c2b7-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="2c2b7-112">Cell name:</span></span>  <br/> |<span data-ttu-id="2c2b7-113">Char.Color[ *i*  ] ここで  *、i*  = <1>、2、3、..</span><span class="sxs-lookup"><span data-stu-id="2c2b7-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="2c2b7-114">プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="2c2b7-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="2c2b7-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="2c2b7-115">Section index:</span></span>  <br/> |<span data-ttu-id="2c2b7-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="2c2b7-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="2c2b7-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="2c2b7-117">Row index:</span></span>  <br/> |<span data-ttu-id="2c2b7-118">**visRowCharacter**  +  *i* *=* 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="2c2b7-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="2c2b7-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="2c2b7-119">Cell index:</span></span>  <br/> |<span data-ttu-id="2c2b7-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="2c2b7-120">**visCharacterColor**</span></span> <br/> |
   

