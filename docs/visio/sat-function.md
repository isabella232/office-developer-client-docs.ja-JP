---
title: SAT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251494
localization_priority: Normal
ms.assetid: 407817fb-9e4a-d2ca-6125-2440d2a417c6
description: 色の彩度コンポーネントの値を返します。
ms.openlocfilehash: 3b3fd8e13ca9af4f0aea00d2f78c7b5c27be1932
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415006"
---
# <a name="sat-function"></a><span data-ttu-id="44d82-103">SAT 関数</span><span class="sxs-lookup"><span data-stu-id="44d82-103">SAT Function</span></span>

<span data-ttu-id="44d82-104">色の彩度コンポーネントの値を返します。</span><span class="sxs-lookup"><span data-stu-id="44d82-104">Returns the value of a color's saturation component.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="44d82-105">構文</span><span class="sxs-lookup"><span data-stu-id="44d82-105">Syntax</span></span>

<span data-ttu-id="44d82-106">SAT(\*\* *式* \*\* )</span><span class="sxs-lookup"><span data-stu-id="44d82-106">SAT(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="44d82-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="44d82-107">Parameters</span></span>

|<span data-ttu-id="44d82-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="44d82-108">**Name**</span></span>|<span data-ttu-id="44d82-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="44d82-109">**Required/Optional**</span></span>|<span data-ttu-id="44d82-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="44d82-110">**Data Type**</span></span>|<span data-ttu-id="44d82-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="44d82-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="44d82-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="44d82-112">_expression_</span></span> <br/> |<span data-ttu-id="44d82-113">必須</span><span class="sxs-lookup"><span data-stu-id="44d82-113">Required</span></span>  <br/> |<span data-ttu-id="44d82-114">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="44d82-114">**Varies**</span></span> <br/> |<span data-ttu-id="44d82-115">引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="44d82-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="44d82-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="44d82-116">Return value</span></span>

<span data-ttu-id="44d82-117">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="44d82-117">Numeric</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44d82-118">注釈</span><span class="sxs-lookup"><span data-stu-id="44d82-118">Remarks</span></span>

<span data-ttu-id="44d82-p101">戻り値は 0 ～ 240 の数値です。入力した引数が無効な場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="44d82-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span>
  
## <a name="example-1"></a><span data-ttu-id="44d82-121">例 1</span><span class="sxs-lookup"><span data-stu-id="44d82-121">Example 1</span></span>

<span data-ttu-id="44d82-122">SAT(Sheet.4!FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="44d82-122">SAT(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="44d82-123">Sheet.4 について、前景の塗りつぶしの色に関する彩度を返します。</span><span class="sxs-lookup"><span data-stu-id="44d82-123">Returns the saturation of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="44d82-124">例 2</span><span class="sxs-lookup"><span data-stu-id="44d82-124">Example 2</span></span>

<span data-ttu-id="44d82-125">SAT(8)</span><span class="sxs-lookup"><span data-stu-id="44d82-125">SAT(8)</span></span>
  
<span data-ttu-id="44d82-126">図面が既定の Visio カラー パレットを使用する場合、240 を返します。Visio カラー パレットでは、インデックス 8 は濃い赤を示します。</span><span class="sxs-lookup"><span data-stu-id="44d82-126">Returns 240 if the document uses the default Visio color palette, where dark red is the color at index 8.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="44d82-127">例 3</span><span class="sxs-lookup"><span data-stu-id="44d82-127">Example 3</span></span>

<span data-ttu-id="44d82-128">SAT(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="44d82-128">SAT(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="44d82-129">20 を返します。</span><span class="sxs-lookup"><span data-stu-id="44d82-129">Returns 20.</span></span>
  

