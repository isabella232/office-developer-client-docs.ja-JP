---
title: BLUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251402
localization_priority: Normal
ms.assetid: da9fb933-4e2c-3e2a-1879-6e70db0cd830
description: 色の青いコンポーネントを返します。 戻り値は、0 ~ 255 の範囲の整数です。含まれています。 入力した引数が無効な場合は、0 を返します。
ms.openlocfilehash: adefbe0f8c2df0ead0f3e50cd5d4945501972865
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439038"
---
# <a name="blue-function"></a><span data-ttu-id="087f8-105">BLUE 関数</span><span class="sxs-lookup"><span data-stu-id="087f8-105">BLUE Function</span></span>

<span data-ttu-id="087f8-106">色の青いコンポーネントを返します。</span><span class="sxs-lookup"><span data-stu-id="087f8-106">Returns the blue component of a color.</span></span> <span data-ttu-id="087f8-107">戻り値は、0 ~ 255 の範囲の整数です。含まれています。</span><span class="sxs-lookup"><span data-stu-id="087f8-107">The return value is an integer in the range of 0 to 255, inclusive.</span></span> <span data-ttu-id="087f8-108">入力した引数が無効な場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="087f8-108">The function returns 0 for invalid input.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="087f8-109">構文</span><span class="sxs-lookup"><span data-stu-id="087f8-109">Syntax</span></span>

<span data-ttu-id="087f8-110">BLUE(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="087f8-110">BLUE(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="087f8-111">パラメーター</span><span class="sxs-lookup"><span data-stu-id="087f8-111">Parameters</span></span>

|<span data-ttu-id="087f8-112">**名前**</span><span class="sxs-lookup"><span data-stu-id="087f8-112">**Name**</span></span>|<span data-ttu-id="087f8-113">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="087f8-113">**Required/Optional**</span></span>|<span data-ttu-id="087f8-114">**データ型**</span><span class="sxs-lookup"><span data-stu-id="087f8-114">**Data Type**</span></span>|<span data-ttu-id="087f8-115">**説明**</span><span class="sxs-lookup"><span data-stu-id="087f8-115">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="087f8-116">_expression_</span><span class="sxs-lookup"><span data-stu-id="087f8-116">_expression_</span></span> <br/> |<span data-ttu-id="087f8-117">必須</span><span class="sxs-lookup"><span data-stu-id="087f8-117">Required</span></span>  <br/> |<span data-ttu-id="087f8-118">**String**</span><span class="sxs-lookup"><span data-stu-id="087f8-118">**String**</span></span> <br/> |<span data-ttu-id="087f8-119">引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="087f8-119">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="087f8-120">戻り値</span><span class="sxs-lookup"><span data-stu-id="087f8-120">Return value</span></span>

<span data-ttu-id="087f8-121">整数</span><span class="sxs-lookup"><span data-stu-id="087f8-121">Integer</span></span>
  
## <a name="example-1"></a><span data-ttu-id="087f8-122">例 1</span><span class="sxs-lookup"><span data-stu-id="087f8-122">Example 1</span></span>

<span data-ttu-id="087f8-123">BLUE(Sheet.4!FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="087f8-123">BLUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="087f8-124">Sheet.4 の前景の塗りつぶしの色に対する青のコンポーネントを返します。</span><span class="sxs-lookup"><span data-stu-id="087f8-124">Returns the blue component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="087f8-125">例 2</span><span class="sxs-lookup"><span data-stu-id="087f8-125">Example 2</span></span>

<span data-ttu-id="087f8-126">BLUE(13)</span><span class="sxs-lookup"><span data-stu-id="087f8-126">BLUE(13)</span></span>
  
<span data-ttu-id="087f8-127">図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、シアンのインデックスは 13 です。</span><span class="sxs-lookup"><span data-stu-id="087f8-127">Returns 128 if the document uses the default Visio color palette, where cyan is the color at index 13.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="087f8-128">例 3</span><span class="sxs-lookup"><span data-stu-id="087f8-128">Example 3</span></span>

<span data-ttu-id="087f8-129">BLUE(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="087f8-129">BLUE(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="087f8-130">30 を返します。</span><span class="sxs-lookup"><span data-stu-id="087f8-130">Returns 30.</span></span>
  

