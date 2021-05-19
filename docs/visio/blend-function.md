---
title: BLEND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: float パラメーターで指定された比率で 2 つの色をブレンドします。
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432787"
---
# <a name="blend-function"></a><span data-ttu-id="5b637-103">BLEND 関数</span><span class="sxs-lookup"><span data-stu-id="5b637-103">BLEND Function</span></span>

<span data-ttu-id="5b637-104">float パラメーターで指定された比率で 2 つの色  _をブレンド_ します。</span><span class="sxs-lookup"><span data-stu-id="5b637-104">Blends two colors in the proportion specified by the  _float_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="5b637-105">構文</span><span class="sxs-lookup"><span data-stu-id="5b637-105">Syntax</span></span>

<span data-ttu-id="5b637-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="5b637-106">BLEND(\*\* *color1* \*\*, \*\* *color2* \*\*, \*\* *float[0,1]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="5b637-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="5b637-107">Parameters</span></span>

|<span data-ttu-id="5b637-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="5b637-108">**Name**</span></span>|<span data-ttu-id="5b637-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="5b637-109">**Required/Optional**</span></span>|<span data-ttu-id="5b637-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="5b637-110">**Data Type**</span></span>|<span data-ttu-id="5b637-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="5b637-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="5b637-112">_color1_</span><span class="sxs-lookup"><span data-stu-id="5b637-112">_color1_</span></span> <br/> |<span data-ttu-id="5b637-113">必須</span><span class="sxs-lookup"><span data-stu-id="5b637-113">Required</span></span>  <br/> |<span data-ttu-id="5b637-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="5b637-114">**Numeric**</span></span> <br/> |<span data-ttu-id="5b637-115">最初の色の Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b637-115">The Visio color index or RGB value of the first color.</span></span>  <br/> |
| <span data-ttu-id="5b637-116">_color2_</span><span class="sxs-lookup"><span data-stu-id="5b637-116">_color2_</span></span> <br/> |<span data-ttu-id="5b637-117">必須</span><span class="sxs-lookup"><span data-stu-id="5b637-117">Required</span></span>  <br/> |<span data-ttu-id="5b637-118">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="5b637-118">**Numeric**</span></span> <br/> |<span data-ttu-id="5b637-119">2 番目の色の Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="5b637-119">The Visio color index or RGB value of the second color.</span></span>  <br/> |
| <span data-ttu-id="5b637-120">_float[0,1]_</span><span class="sxs-lookup"><span data-stu-id="5b637-120">_float[0,1]_</span></span> <br/> |<span data-ttu-id="5b637-121">必須</span><span class="sxs-lookup"><span data-stu-id="5b637-121">Required</span></span>  <br/> |<span data-ttu-id="5b637-122">**Float**</span><span class="sxs-lookup"><span data-stu-id="5b637-122">**Float**</span></span> <br/> |<span data-ttu-id="5b637-123">color2 と  _color1_ をそれぞれブレンド  _する_ 比率。</span><span class="sxs-lookup"><span data-stu-id="5b637-123">The proportion in which to blend  _color2_ and  _color1_, respectively.</span></span> <span data-ttu-id="5b637-124">0 ～ 1 の実数を使用します。</span><span class="sxs-lookup"><span data-stu-id="5b637-124">A real number from 0 to 1 inclusive.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="5b637-125">戻り値</span><span class="sxs-lookup"><span data-stu-id="5b637-125">Return value</span></span>

 <span data-ttu-id="5b637-126">**RGB**</span><span class="sxs-lookup"><span data-stu-id="5b637-126">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5b637-127">注釈</span><span class="sxs-lookup"><span data-stu-id="5b637-127">Remarks</span></span>

<span data-ttu-id="5b637-128">返される色は、float パラメーターで指定された色  _2_ と  _色 1_ をそれぞれブレンドする相対的な比率  _によって決_ まります。</span><span class="sxs-lookup"><span data-stu-id="5b637-128">The color returned is determined by the relative proportions in which to blend  _color2_ and  _color1_, respectively, as specified by the  _float_ parameter.</span></span> <span data-ttu-id="5b637-129">たとえば  _、float_ が 0.25 の場合、返される色は  _color1_ の 75% と  _color2_ の 25% で構成されます。</span><span class="sxs-lookup"><span data-stu-id="5b637-129">For example, if  _float_ is 0.25, the color returned is composed 75% of  _color1_ and 25% of  _color2_.</span></span> 
  
<span data-ttu-id="5b637-130">もう 1 つの考え方は、  _浮動小数点_ 値が  _color1_ から color2 の色スペクトルに沿った点に対応  _する点です_。</span><span class="sxs-lookup"><span data-stu-id="5b637-130">Another way to think about it is that the  _float_ value corresponds to the point along the color spectrum from  _color1_ to  _color2_.</span></span> <span data-ttu-id="5b637-131">したがって、浮動小数点数の小さい数値 (ゼロに近い) は色 _1_ に近いブレンドを生成し、より大きな数値 (1 に近い) は _color2_ に近いブレンドを生成します。</span><span class="sxs-lookup"><span data-stu-id="5b637-131">Therefore, smaller numbers (closer to zero) for  _float_ produce blends closer to  _color1_, while larger numbers (closer to 1) produce blends closer to  _color2_.</span></span>
  

