---
title: '[Color] セル ([Layers] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm165
localization_priority: Normal
ms.assetid: 61c19342-46fb-48d4-6375-c9ea8306286d
description: レイヤーの表示に使用する色を指定します。
ms.openlocfilehash: b6728d44c71f6403e772a6a7e730ba3c18d9eb48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805024"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="81c32-103">[Color] セル ([レイヤー] セクション)</span><span class="sxs-lookup"><span data-stu-id="81c32-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="81c32-104">レイヤーの表示に使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="81c32-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="81c32-105">注釈</span><span class="sxs-lookup"><span data-stu-id="81c32-105">Remarks</span></span>

<span data-ttu-id="81c32-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="81c32-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="81c32-107">このセルの値は、 **[レイヤー プロパティ**] ダイアログ ボックスで**レイヤーの色**の設定に対応する ([**ホーム**] タブの [**編集**]、[**レイヤー** ] をクリックし、[**レイヤー プロパティ**] をクリック) します。</span><span class="sxs-lookup"><span data-stu-id="81c32-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="81c32-108">独自の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="81c32-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="81c32-109">その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。</span><span class="sxs-lookup"><span data-stu-id="81c32-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="81c32-110">数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。</span><span class="sxs-lookup"><span data-stu-id="81c32-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="81c32-111">255 の値は、レイヤーに色が含まれていないことを示します。</span><span class="sxs-lookup"><span data-stu-id="81c32-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="81c32-112">レイヤーの色の透過性を設定するには、[Transparency] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="81c32-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="81c32-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="81c32-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81c32-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="81c32-114">Cell name:</span></span>  <br/> |<span data-ttu-id="81c32-115">Layers.Color [ *i* ]、 *i* = < 1 > では、2、3、.</span><span class="sxs-lookup"><span data-stu-id="81c32-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="81c32-116">プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="81c32-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="81c32-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="81c32-117">Section index:</span></span>  <br/> |<span data-ttu-id="81c32-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="81c32-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="81c32-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="81c32-119">Row index:</span></span>  <br/> |<span data-ttu-id="81c32-120">**visRowLayer** +  *i* 、 *i* = 0、1、2、.</span><span class="sxs-lookup"><span data-stu-id="81c32-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="81c32-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="81c32-121">Cell index:</span></span>  <br/> |<span data-ttu-id="81c32-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="81c32-122">**visLayerColor**</span></span> <br/> |
   

