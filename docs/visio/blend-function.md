---
title: BLEND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Float 型パラメーターで指定された比率で 2 つの色をブレンドします。
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804899"
---
# <a name="blend-function"></a><span data-ttu-id="c6dcb-103">BLEND 関数</span><span class="sxs-lookup"><span data-stu-id="c6dcb-103">BLEND Function</span></span>

<span data-ttu-id="c6dcb-104">_Float 型_パラメーターで指定された比率で 2 つの色をブレンドします。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c6dcb-105">構文</span><span class="sxs-lookup"><span data-stu-id="c6dcb-105">Syntax</span></span>

<span data-ttu-id="c6dcb-106">ブレンド (* * *color1* * *、* * *color2* * *、* * *[0, 1] の浮動小数点数** *)</span><span class="sxs-lookup"><span data-stu-id="c6dcb-106">BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c6dcb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c6dcb-107">Parameters</span></span>

|<span data-ttu-id="c6dcb-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-108">**Name**</span></span>|<span data-ttu-id="c6dcb-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-109">**Required/Optional**</span></span>|<span data-ttu-id="c6dcb-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-110">**Data Type**</span></span>|<span data-ttu-id="c6dcb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c6dcb-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="c6dcb-112">_color1_</span></span> <br/> |<span data-ttu-id="c6dcb-113">必須</span><span class="sxs-lookup"><span data-stu-id="c6dcb-113">Required</span></span>  <br/> |<span data-ttu-id="c6dcb-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c6dcb-115">最初の色の Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="c6dcb-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="c6dcb-116">_color2_</span></span> <br/> |<span data-ttu-id="c6dcb-117">必須</span><span class="sxs-lookup"><span data-stu-id="c6dcb-117">Required</span></span>  <br/> |<span data-ttu-id="c6dcb-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-118">**Numeric**</span></span> <br/> |<span data-ttu-id="c6dcb-119">2 番目の色の Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="c6dcb-120">_float [0, 1]_</span><span class="sxs-lookup"><span data-stu-id="c6dcb-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="c6dcb-121">必須</span><span class="sxs-lookup"><span data-stu-id="c6dcb-121">Required</span></span>  <br/> |<span data-ttu-id="c6dcb-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-122">**Float**</span></span> <br/> |<span data-ttu-id="c6dcb-123">_Color2_と_color1_をそれぞれブレンドする割合。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="c6dcb-124">実数 0 ~ 1 にします。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c6dcb-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="c6dcb-125">Return value</span></span>

 <span data-ttu-id="c6dcb-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="c6dcb-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c6dcb-127">注釈</span><span class="sxs-lookup"><span data-stu-id="c6dcb-127">Remarks</span></span>

<span data-ttu-id="c6dcb-128">返される色は、 _color2_と_color1_のそれぞれに、_浮動小数点_パラメーターで指定されているブレンドするための相対的比率によって決定されます。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="c6dcb-129">_Float_が 0.25 の場合は、返されるカラーは構成の 75% の_color1_と_color2_の 25% です。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="c6dcb-130">考える別の方法では、 _color2_に_color1_のカラー スペクトルに沿ってポイントを_float 型_の値が対応します。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="c6dcb-131">したがって、小さい番号 (0 に近い)_浮動小数点数_の生成ブレンド近くするには_color1_、大きい数値 (1 に近い) 中に生成_color2_に近い場所にブレンド用です。</span><span class="sxs-lookup"><span data-stu-id="c6dcb-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

