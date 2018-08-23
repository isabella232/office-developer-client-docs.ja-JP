---
title: HUE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251440
localization_priority: Normal
ms.assetid: 0f5c6097-eef5-5f58-e2ef-2c348e42dc9a
description: 色の色合いコンポーネントの値を返します。
ms.openlocfilehash: 2a532e305eb7cbabc5ba07dcace6c07a337e7743
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805542"
---
# <a name="hue-function"></a><span data-ttu-id="96cb7-103">HUE 関数</span><span class="sxs-lookup"><span data-stu-id="96cb7-103">HUE Function</span></span>

<span data-ttu-id="96cb7-104">色の色合いコンポーネントの値を返します。</span><span class="sxs-lookup"><span data-stu-id="96cb7-104">Returns the value of a color's hue component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="96cb7-105">構文</span><span class="sxs-lookup"><span data-stu-id="96cb7-105">Syntax</span></span>

<span data-ttu-id="96cb7-106">色相 (* **式** *)</span><span class="sxs-lookup"><span data-stu-id="96cb7-106">HUE(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="96cb7-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="96cb7-107">Parameters</span></span>

|<span data-ttu-id="96cb7-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="96cb7-108">**Name**</span></span>|<span data-ttu-id="96cb7-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="96cb7-109">**Required/Optional**</span></span>|<span data-ttu-id="96cb7-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="96cb7-110">**Data Type**</span></span>|<span data-ttu-id="96cb7-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="96cb7-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="96cb7-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="96cb7-112">_expression_</span></span> <br/> |<span data-ttu-id="96cb7-113">必須</span><span class="sxs-lookup"><span data-stu-id="96cb7-113">Required</span></span>  <br/> |<span data-ttu-id="96cb7-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="96cb7-114">**String**</span></span> <br/> |<span data-ttu-id="96cb7-115">色として評価される式を指定します。</span><span class="sxs-lookup"><span data-stu-id="96cb7-115">An expression that evaluates to a color.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="96cb7-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="96cb7-116">Return value</span></span>

<span data-ttu-id="96cb7-117">数値</span><span class="sxs-lookup"><span data-stu-id="96cb7-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="96cb7-118">注釈</span><span class="sxs-lookup"><span data-stu-id="96cb7-118">Remarks</span></span>

<span data-ttu-id="96cb7-p101">戻り値は 0 ～ 239 の数値です。引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。入力した引数が無効な場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="96cb7-p101">The return value is a number in the range 0 to 239, inclusive. The input is an index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="96cb7-122">例 1</span><span class="sxs-lookup"><span data-stu-id="96cb7-122">Example 1</span></span>

<span data-ttu-id="96cb7-123">色相 (Sheet.4!FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="96cb7-123">HUE(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="96cb7-124">Sheet.4 について、前景の塗りつぶしの色に関する色合いを返します。</span><span class="sxs-lookup"><span data-stu-id="96cb7-124">Returns the hue of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="96cb7-125">例 2</span><span class="sxs-lookup"><span data-stu-id="96cb7-125">Example 2</span></span>

<span data-ttu-id="96cb7-126">HUE(7)</span><span class="sxs-lookup"><span data-stu-id="96cb7-126">HUE(7)</span></span>
  
<span data-ttu-id="96cb7-127">図面で既定の Microsoft Visio カラー パレットを使用する場合、120 を返します。Visio カラー パレットでは、インデックス 7 はシアンを示します。</span><span class="sxs-lookup"><span data-stu-id="96cb7-127">Returns 120 if the document uses the default Microsoft Visio color palette, where cyan is the color at index 7.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="96cb7-128">例 3</span><span class="sxs-lookup"><span data-stu-id="96cb7-128">Example 3</span></span>

<span data-ttu-id="96cb7-129">HUE(HSL(10, 20, 30) )</span><span class="sxs-lookup"><span data-stu-id="96cb7-129">HUE(HSL(10, 20, 30) )</span></span>
  
<span data-ttu-id="96cb7-130">10 を返します。</span><span class="sxs-lookup"><span data-stu-id="96cb7-130">Returns 10.</span></span>
  

