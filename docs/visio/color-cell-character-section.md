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
ms.openlocfilehash: ef07f4165882e08a2292e4ee549f8807fe8403e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805007"
---
# <a name="color-cell-character-section"></a><span data-ttu-id="64882-103">[Color] セル ([文字] セクション)</span><span class="sxs-lookup"><span data-stu-id="64882-103">Color Cell (Character Section)</span></span>

<span data-ttu-id="64882-104">図形のテキストに使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="64882-104">Determines the color used for the shape's text.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="64882-105">注釈</span><span class="sxs-lookup"><span data-stu-id="64882-105">Remarks</span></span>

<span data-ttu-id="64882-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="64882-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="64882-107">独自の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="64882-107">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="64882-108">その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="64882-108">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="64882-109">数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。</span><span class="sxs-lookup"><span data-stu-id="64882-109">When used in numeric operations, custom colors have values of 24 and above.</span></span> 
  
<span data-ttu-id="64882-110">テキストの色の透過性を設定するには、[Transparency] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="64882-110">You can set the transparency of the text color in the Transparency cell.</span></span>
  
<span data-ttu-id="64882-111">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="64882-111">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64882-112">セル名:</span><span class="sxs-lookup"><span data-stu-id="64882-112">Cell name:</span></span>  <br/> |<span data-ttu-id="64882-113">Char.Color [ *i* ]、 *i* = < 1 > では、2、3、.</span><span class="sxs-lookup"><span data-stu-id="64882-113">Char.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="64882-114">プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="64882-114">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="64882-115">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="64882-115">Section index:</span></span>  <br/> |<span data-ttu-id="64882-116">**visSectionCharacter**</span><span class="sxs-lookup"><span data-stu-id="64882-116">**visSectionCharacter**</span></span> <br/> |
|<span data-ttu-id="64882-117">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="64882-117">Row index:</span></span>  <br/> |<span data-ttu-id="64882-118">**visRowCharacter** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="64882-118">**visRowCharacter** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="64882-119">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="64882-119">Cell index:</span></span>  <br/> |<span data-ttu-id="64882-120">**visCharacterColor**</span><span class="sxs-lookup"><span data-stu-id="64882-120">**visCharacterColor**</span></span> <br/> |
   

