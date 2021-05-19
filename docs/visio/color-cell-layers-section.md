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
ms.openlocfilehash: a2eef24187165cabfdfc8dee49747a2381562d3e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435132"
---
# <a name="color-cell-layers-section"></a><span data-ttu-id="d1600-103">[Color] セル ([Layers] セクション)</span><span class="sxs-lookup"><span data-stu-id="d1600-103">Color Cell (Layers Section)</span></span>

<span data-ttu-id="d1600-104">レイヤーの表示に使用する色を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1600-104">Specifies the color used to display the layer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1600-105">注釈</span><span class="sxs-lookup"><span data-stu-id="d1600-105">Remarks</span></span>

<span data-ttu-id="d1600-106">色を設定するには、0 ～ 23 の数値を入力します。</span><span class="sxs-lookup"><span data-stu-id="d1600-106">To set the color, enter a number from 0 to 23.</span></span>
  
<span data-ttu-id="d1600-107">このセル値は、[レイヤープロパティ] ダイアログボックスの [レイヤーの色] 設定に対応します ([ホーム] タブの [編集] グループで、[レイヤー] をクリックし、[レイヤー プロパティ] を **クリックします**)。 </span><span class="sxs-lookup"><span data-stu-id="d1600-107">This cell value corresponds to the **Layer color** setting in the **Layer Properties** dialog box (in the **Editing** group on the **Home** tab, click **Layers** and then click **Layer Properties**).</span></span>
  
<span data-ttu-id="d1600-108">ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1600-108">To enter a custom color, use the RGB or HSL function.</span></span> <span data-ttu-id="d1600-109">カスタム色の値は RGB 色で、数値ではなく RGB( *r, g, b*) が ShapeSheet ウィンドウに表示されます。</span><span class="sxs-lookup"><span data-stu-id="d1600-109">The value of a custom color is its RGB color, and RGB( *r, g, b*), rather than a number, will be shown in the ShapeSheet window.</span></span> <span data-ttu-id="d1600-110">ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1600-110">When used in numeric operations, custom colors have values of 24 and above.</span></span> <span data-ttu-id="d1600-111">値 255 は、そのレイヤーが無色であることを示します。</span><span class="sxs-lookup"><span data-stu-id="d1600-111">A value of 255 indicates that the layer has no color.</span></span> 
  
<span data-ttu-id="d1600-112">レイヤーの色の透過性を設定するには、[Transparency] セルを使用します。</span><span class="sxs-lookup"><span data-stu-id="d1600-112">You can set the transparency of the layer color in the Transparency cell.</span></span>
  
<span data-ttu-id="d1600-113">別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。</span><span class="sxs-lookup"><span data-stu-id="d1600-113">To get a reference to the Color cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1600-114">セル名:</span><span class="sxs-lookup"><span data-stu-id="d1600-114">Cell name:</span></span>  <br/> |<span data-ttu-id="d1600-115">Layers.Color[ *i*  ] ここで  *、i*  = <1>、2、3、..</span><span class="sxs-lookup"><span data-stu-id="d1600-115">Layers.Color[ *i*  ]           where  *i*  = <1>, 2, 3, ...</span></span>  <br/> |
   
<span data-ttu-id="d1600-116">プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。</span><span class="sxs-lookup"><span data-stu-id="d1600-116">To get a reference to the Color cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="d1600-117">セクション インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1600-117">Section index:</span></span>  <br/> |<span data-ttu-id="d1600-118">**visSectionLayer**</span><span class="sxs-lookup"><span data-stu-id="d1600-118">**visSectionLayer**</span></span> <br/> |
|<span data-ttu-id="d1600-119">行インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1600-119">Row index:</span></span>  <br/> |<span data-ttu-id="d1600-120">**visRowLayer**  +  *i* *=* 0, 1, 2, ...</span><span class="sxs-lookup"><span data-stu-id="d1600-120">**visRowLayer** +  *i*           where  *i*  = 0, 1, 2, ...</span></span>  <br/> |
|<span data-ttu-id="d1600-121">セル インデックス:</span><span class="sxs-lookup"><span data-stu-id="d1600-121">Cell index:</span></span>  <br/> |<span data-ttu-id="d1600-122">**visLayerColor**</span><span class="sxs-lookup"><span data-stu-id="d1600-122">**visLayerColor**</span></span> <br/> |
   

