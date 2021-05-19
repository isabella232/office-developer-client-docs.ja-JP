---
title: LUM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251460
localization_priority: Normal
ms.assetid: 38e6bba7-1bf2-3d31-0912-707002454f5d
description: 色の光度コンポーネントの値を返します。
ms.openlocfilehash: 17fa43f8e2cd7422428f92724e351436233c2d62
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419339"
---
# <a name="lum-function"></a><span data-ttu-id="dfa0e-103">LUM 関数</span><span class="sxs-lookup"><span data-stu-id="dfa0e-103">LUM Function</span></span>

<span data-ttu-id="dfa0e-104">色の光度コンポーネントの値を返します。</span><span class="sxs-lookup"><span data-stu-id="dfa0e-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="dfa0e-105">構文</span><span class="sxs-lookup"><span data-stu-id="dfa0e-105">Syntax</span></span>

<span data-ttu-id="dfa0e-106">LUM(\*\* *expression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="dfa0e-106">LUM(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="dfa0e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="dfa0e-107">Parameters</span></span>

|<span data-ttu-id="dfa0e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="dfa0e-108">**Name**</span></span>|<span data-ttu-id="dfa0e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="dfa0e-109">**Required/Optional**</span></span>|<span data-ttu-id="dfa0e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="dfa0e-110">**Data Type**</span></span>|<span data-ttu-id="dfa0e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="dfa0e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="dfa0e-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="dfa0e-112">_expression_</span></span> <br/> |<span data-ttu-id="dfa0e-113">必須</span><span class="sxs-lookup"><span data-stu-id="dfa0e-113">Required</span></span>  <br/> |<span data-ttu-id="dfa0e-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="dfa0e-114">**Numeric**</span></span> <br/> |<span data-ttu-id="dfa0e-115">図面のカラー テーブルにある色のインデックス、またはカラー インデックスを含むセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="dfa0e-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="dfa0e-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="dfa0e-116">Return value</span></span>

<span data-ttu-id="dfa0e-117">番号</span><span class="sxs-lookup"><span data-stu-id="dfa0e-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="dfa0e-118">注釈</span><span class="sxs-lookup"><span data-stu-id="dfa0e-118">Remarks</span></span>

<span data-ttu-id="dfa0e-p101">戻り値は 0 ～ 240 の数値です。入力した引数が無効な場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="dfa0e-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="dfa0e-121">例 1</span><span class="sxs-lookup"><span data-stu-id="dfa0e-121">Example 1</span></span>

<span data-ttu-id="dfa0e-122">LUM(Sheet.4!FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="dfa0e-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="dfa0e-123">Sheet.4 について、前景の塗りつぶしの色に関する明度を返します。</span><span class="sxs-lookup"><span data-stu-id="dfa0e-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="dfa0e-124">例 2</span><span class="sxs-lookup"><span data-stu-id="dfa0e-124">Example 2</span></span>

<span data-ttu-id="dfa0e-125">LUM(6)</span><span class="sxs-lookup"><span data-stu-id="dfa0e-125">LUM(6)</span></span>
  
<span data-ttu-id="dfa0e-126">図面が既定の Visio カラー パレットを使用する場合、120 を返します。Visio カラー パレットでは、インデックス 6 はマゼンタを示します。</span><span class="sxs-lookup"><span data-stu-id="dfa0e-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="dfa0e-127">例 3</span><span class="sxs-lookup"><span data-stu-id="dfa0e-127">Example 3</span></span>

<span data-ttu-id="dfa0e-128">LUM(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="dfa0e-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="dfa0e-129">30 を返します。</span><span class="sxs-lookup"><span data-stu-id="dfa0e-129">Returns 30.</span></span>
  

