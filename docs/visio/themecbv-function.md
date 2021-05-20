---
title: THEMECBV 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ef62f63f-b2ce-4d12-a294-93dbdc9a869d
description: 引数として渡される色 (数値) が、アクティブなテーマのグラデーション設定に格納されている指定された濃色または濃色の値によって変更された、ドキュメントのカラー パレット内のインデックスを表す RGB 値または整数を返します。
ms.openlocfilehash: 014dc04c5114e296cd2226f3cf04dfb729817578
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429139"
---
# <a name="themecbv-function"></a><span data-ttu-id="d933f-103">THEMECBV 関数</span><span class="sxs-lookup"><span data-stu-id="d933f-103">THEMECBV Function</span></span>

<span data-ttu-id="d933f-104">引数として渡される色 (数値) が、アクティブなテーマのグラデーション設定に格納されている指定された濃色または濃色の値によって変更された、ドキュメントのカラー パレット内のインデックスを表す RGB 値または整数を返します。</span><span class="sxs-lookup"><span data-stu-id="d933f-104">Returns an RGB value or an integer that represents an index in the document's color palette, where the color (number) passed in as an argument has been modified by the specified tint or shade value stored in the gradient settings of the active theme.</span></span> 
  
## <a name="version-information"></a><span data-ttu-id="d933f-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="d933f-105">Version Information</span></span>

<span data-ttu-id="d933f-106">追加バージョン: Visio 2013
</span><span class="sxs-lookup"><span data-stu-id="d933f-106">Version Added: Visio 2013</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d933f-107">構文</span><span class="sxs-lookup"><span data-stu-id="d933f-107">Syntax</span></span>

 <span data-ttu-id="d933f-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span><span class="sxs-lookup"><span data-stu-id="d933f-108">**THEMECBV**( _color_,  _gradient_stop_number_)</span></span>
  
### <a name="parameters"></a><span data-ttu-id="d933f-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d933f-109">Parameters</span></span>

|<span data-ttu-id="d933f-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="d933f-110">**Name**</span></span>|<span data-ttu-id="d933f-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d933f-111">**Required/Optional**</span></span>|<span data-ttu-id="d933f-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d933f-112">**Data Type**</span></span>|<span data-ttu-id="d933f-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="d933f-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d933f-114">_color_</span><span class="sxs-lookup"><span data-stu-id="d933f-114">_color_</span></span> <br/> |<span data-ttu-id="d933f-115">必須</span><span class="sxs-lookup"><span data-stu-id="d933f-115">Required</span></span>  <br/> |<span data-ttu-id="d933f-116">**数値**</span><span class="sxs-lookup"><span data-stu-id="d933f-116">**Number**</span></span> <br/> |<span data-ttu-id="d933f-117">ドキュメントのカラー パレット内のインデックスを表す数値。</span><span class="sxs-lookup"><span data-stu-id="d933f-117">A number representing an index in the document's color palette.</span></span>  <br/> |
| <span data-ttu-id="d933f-118">_gradient_stop_number_</span><span class="sxs-lookup"><span data-stu-id="d933f-118">_gradient_stop_number_</span></span> <br/> |<span data-ttu-id="d933f-119">必須</span><span class="sxs-lookup"><span data-stu-id="d933f-119">Required</span></span>  <br/> |<span data-ttu-id="d933f-120">**数値**</span><span class="sxs-lookup"><span data-stu-id="d933f-120">**Number**</span></span> <br/> |<span data-ttu-id="d933f-121">色に適用する、アクティブなテーマのグラデーションの設定に格納された、グラデーションの分岐点 (濃淡または網かけ)。</span><span class="sxs-lookup"><span data-stu-id="d933f-121">The gradient stop (tint or shade) stored in the gradient settings of the active theme to apply to the color.</span></span>  <br/> |
   
## <a name="return-value"></a><span data-ttu-id="d933f-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="d933f-122">Return value</span></span>

 <span data-ttu-id="d933f-123">**数値**</span><span class="sxs-lookup"><span data-stu-id="d933f-123">**Number**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d933f-124">注釈</span><span class="sxs-lookup"><span data-stu-id="d933f-124">Remarks</span></span>

> [!NOTE]
> <span data-ttu-id="d933f-125">THEMECBV 関数は、図形に割り当てられた QuickStyle にグラデーションが設定されていない場合、引数として渡される色には何もしません。</span><span class="sxs-lookup"><span data-stu-id="d933f-125">The THEMECBV function does nothing to the color passed in as an argument if the QuickStyle that is assigned to the shape does not have a gradient.</span></span> 
  
<span data-ttu-id="d933f-126">テーマのグラデーション設定は、"明るくなる" (濃淡) または "濃淡" (日陰) に対応する一連の番号付きグラデーションストップです。</span><span class="sxs-lookup"><span data-stu-id="d933f-126">The gradient settings in a theme are a series of numbered gradient stops that correspond to a "lightening" (tint) or "darkening" (shade).</span></span> <span data-ttu-id="d933f-127">これらの暗さと明るさは、グラデーションの色効果を作成するために、基本色に適用されます。</span><span class="sxs-lookup"><span data-stu-id="d933f-127">These shades and tints are applied to a base color to create a gradient color effect.</span></span>
  
<span data-ttu-id="d933f-128">**THEMECBV** 関数は、カラー入力を使用して、指定のグラデーションの分岐点の濃淡または網かけによって変更された後の色を出力します。</span><span class="sxs-lookup"><span data-stu-id="d933f-128">The **THEMECBV** function takes a color input and outputs the color after it has been modified by the tint or shade of the specified gradient stop.</span></span> <span data-ttu-id="d933f-129">現在のクイック スタイルにグラデーションの塗りつぶしが含まれている場合、色や色合いはテーマの定義から取得されます。</span><span class="sxs-lookup"><span data-stu-id="d933f-129">The tints and shades come from the theme's definition, if the current quick style contains a gradient fill.</span></span> <span data-ttu-id="d933f-130">アクティブなクイック スタイルでグラデーションの塗りつぶしが指定されていない場合、または図形にテーマが設定されていない場合、この数式によって最初の引数に渡された色が返されます。</span><span class="sxs-lookup"><span data-stu-id="d933f-130">If the active Quick Style does not specify a gradient fill or the shape is set to No Theme, then this formula simply returns the color that was passed in for the first argument.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d933f-131">例</span><span class="sxs-lookup"><span data-stu-id="d933f-131">Example</span></span>

 `THEMECBV(FillForegnd, 5)`
  
<span data-ttu-id="d933f-132">[**FillForegnd**] セルで指定した色へのグラデーションの、グラデーションの 5 番目の分岐点に、濃淡または網かけを適用することで作成された色を返します。</span><span class="sxs-lookup"><span data-stu-id="d933f-132">Returns the color created by applying the tint or shade in the fifth gradient stop of the gradient to the color specified in the **FillForegnd** cell.</span></span> 
  
 `THEMECBV(RGB(255,0,0), 2)`
  
<span data-ttu-id="d933f-133">グラデーションの 2 番目の分岐点を赤の基本色に適用することで作成された、赤の網かけまたは濃淡が返されます。</span><span class="sxs-lookup"><span data-stu-id="d933f-133">Returns a shade or tint of red created by applying the second gradient stop to a base color of red.</span></span>
  

