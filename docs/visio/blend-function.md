---
title: BLEND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: float パラメーターで指定された比率で2つの色を合成します。
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432787"
---
# <a name="blend-function"></a><span data-ttu-id="144ba-103">BLEND 関数</span><span class="sxs-lookup"><span data-stu-id="144ba-103">BLEND Function</span></span>

<span data-ttu-id="144ba-104">_float_パラメーターで指定された比率で2つの色を合成します。</span><span class="sxs-lookup"><span data-stu-id="144ba-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="144ba-105">構文</span><span class="sxs-lookup"><span data-stu-id="144ba-105">Syntax</span></span>

<span data-ttu-id="144ba-106">BLEND (\* \* *color1* \* *、* \* *color2* \* *、* \* *float [0, 1]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="144ba-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="144ba-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="144ba-107">Parameters</span></span>

|<span data-ttu-id="144ba-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="144ba-108">**Name**</span></span>|<span data-ttu-id="144ba-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="144ba-109">**Required/Optional**</span></span>|<span data-ttu-id="144ba-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="144ba-110">**Data Type**</span></span>|<span data-ttu-id="144ba-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="144ba-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="144ba-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="144ba-112">_color1_</span></span> <br/> |<span data-ttu-id="144ba-113">必須</span><span class="sxs-lookup"><span data-stu-id="144ba-113">Required</span></span>  <br/> |<span data-ttu-id="144ba-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="144ba-114">**Numeric**</span></span> <br/> |<span data-ttu-id="144ba-115">最初の色の Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="144ba-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="144ba-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="144ba-116">_color2_</span></span> <br/> |<span data-ttu-id="144ba-117">必須</span><span class="sxs-lookup"><span data-stu-id="144ba-117">Required</span></span>  <br/> |<span data-ttu-id="144ba-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="144ba-118">**Numeric**</span></span> <br/> |<span data-ttu-id="144ba-119">2 番目の色の Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="144ba-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="144ba-120">_float [0, 1]_</span><span class="sxs-lookup"><span data-stu-id="144ba-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="144ba-121">必須</span><span class="sxs-lookup"><span data-stu-id="144ba-121">Required</span></span>  <br/> |<span data-ttu-id="144ba-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="144ba-122">**Float**</span></span> <br/> |<span data-ttu-id="144ba-123">_color2_と_color1_をそれぞれブレンドする比率を指定します。</span><span class="sxs-lookup"><span data-stu-id="144ba-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="144ba-124">0 ～ 1 の実数を使用します。</span><span class="sxs-lookup"><span data-stu-id="144ba-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="144ba-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="144ba-125">Return value</span></span>

 <span data-ttu-id="144ba-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="144ba-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="144ba-127">注釈</span><span class="sxs-lookup"><span data-stu-id="144ba-127">Remarks</span></span>

<span data-ttu-id="144ba-128">返される色は、 _float_パラメーターで指定されたように、 _color2_と_color1_をそれぞれブレンディングする相対的な比率によって決まります。</span><span class="sxs-lookup"><span data-stu-id="144ba-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="144ba-129">たとえば、 _float_が0.25 の場合、返される色は_color1_の 75%、 _color2_の 25% で構成されます。</span><span class="sxs-lookup"><span data-stu-id="144ba-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="144ba-130">この点を考慮するもう1つの方法は、_浮動小数点_値が、 _color1_から_color2_へのカラースペクトルに沿った点に対応していることです。</span><span class="sxs-lookup"><span data-stu-id="144ba-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="144ba-131">そのため、_浮動小数点型_( _color1_) の値が小さいほど、より大きな数値 (1 に近い) は、 _color2_に近い値になります。</span><span class="sxs-lookup"><span data-stu-id="144ba-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

