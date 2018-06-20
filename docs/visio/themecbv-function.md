---
title: THEMECBV 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: グラデーションのテーマの設定に格納されている指定の濃淡または網掛けの値を引数として渡されたカラー (番号) が変更されて、RGB 値またはドキュメントのカラー パレットのインデックスを表す整数を返します。
ms.openlocfilehash: 878da505a840234445d3e16d3b8a68e31eaf5fda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806649"
---
# <a name="themecbv-function"></a><span data-ttu-id="36f76-103">THEMECBV 関数</span><span class="sxs-lookup"><span data-stu-id="36f76-103">THEMECBV Function</span></span>

<span data-ttu-id="36f76-104">グラデーションのテーマの設定に格納されている指定の濃淡または網掛けの値を引数として渡されたカラー (番号) が変更されて、RGB 値またはドキュメントのカラー パレットのインデックスを表す整数を返します。</span><span class="sxs-lookup"><span data-stu-id="36f76-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="36f76-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="36f76-105">Version Information</span></span>

<span data-ttu-id="36f76-106">Visio 2013 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="36f76-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="36f76-107">構文</span><span class="sxs-lookup"><span data-stu-id="36f76-107">Syntax</span></span>

 <span data-ttu-id="36f76-108">**THEMECBV**(_カラー_、 _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="36f76-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="36f76-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="36f76-109">Parameters</span></span>

|<span data-ttu-id="36f76-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="36f76-110">**Name**</span></span>|<span data-ttu-id="36f76-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="36f76-111">**Required/Optional**</span></span>|<span data-ttu-id="36f76-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="36f76-112">**Data Type**</span></span>|<span data-ttu-id="36f76-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="36f76-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="36f76-114">_color_</span><span class="sxs-lookup"><span data-stu-id="36f76-114">_color_</span></span> <br/> |<span data-ttu-id="36f76-115">必須</span><span class="sxs-lookup"><span data-stu-id="36f76-115">Required</span></span>  <br/> |<span data-ttu-id="36f76-116">**番号**</span><span class="sxs-lookup"><span data-stu-id="36f76-116">**Number**</span></span> <br/> |<span data-ttu-id="36f76-117">ドキュメントのカラー パレット内のインデックスを表す数値。</span><span class="sxs-lookup"><span data-stu-id="36f76-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="36f76-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="36f76-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="36f76-119">必須</span><span class="sxs-lookup"><span data-stu-id="36f76-119">Required</span></span>  <br/> |<span data-ttu-id="36f76-120">**番号**</span><span class="sxs-lookup"><span data-stu-id="36f76-120">**Number**</span></span> <br/> |<span data-ttu-id="36f76-121">色に適用する、アクティブなテーマのグラデーションの設定に格納された、グラデーションの分岐点 (濃淡または網かけ)。</span><span class="sxs-lookup"><span data-stu-id="36f76-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="36f76-122">�߂�l</span><span class="sxs-lookup"><span data-stu-id="36f76-122">Return value</span></span>

 <span data-ttu-id="36f76-123">**番号**</span><span class="sxs-lookup"><span data-stu-id="36f76-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="36f76-124">備考</span><span class="sxs-lookup"><span data-stu-id="36f76-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="36f76-125">THEMECBV 関数では、図形に割り当てられている QuickStyle でグラデーションを設定していない場合、引数として渡された色にしません。</span><span class="sxs-lookup"><span data-stu-id="36f76-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="36f76-126">テーマでグラデーションの設定は、一連の「稲妻」(濃淡) と「暗く」(網掛け) に対応する番号付きのグラデーション終了位置です。</span><span class="sxs-lookup"><span data-stu-id="36f76-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="36f76-127">これらの網掛けまたは濃淡は、色のグラデーション効果を作成する基本の色に適用されます。</span><span class="sxs-lookup"><span data-stu-id="36f76-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="36f76-128">**THEMECBV**関数はカラー入力し、指定したグラデーションの分岐点の網掛けまたは濃淡で変更された後に、色を出力します。</span><span class="sxs-lookup"><span data-stu-id="36f76-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="36f76-129">濃淡と網掛けは、現在のクイック スタイルには、グラデーションの塗りつぶしが含まれている場合は、テーマの定義から取得されます。</span><span class="sxs-lookup"><span data-stu-id="36f76-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="36f76-130">アクティブなクイック スタイルにグラデーションの塗りつぶしまたは図形にテーマなしに設定が指定しない場合、この数式は、最初の引数で渡されたカラーを単に返します。</span><span class="sxs-lookup"><span data-stu-id="36f76-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="36f76-131">例</span><span class="sxs-lookup"><span data-stu-id="36f76-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="36f76-132">**FillForegnd** ] セルに指定した色にグラデーションの 5 番目のグラデーション終了位置の網掛けまたは濃淡を適用することによって作成された色を返します。</span><span class="sxs-lookup"><span data-stu-id="36f76-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="36f76-133">グラデーションの 2 番目の分岐点を赤の基本色に適用することで作成された、赤の網かけまたは濃淡が返されます。</span><span class="sxs-lookup"><span data-stu-id="36f76-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

