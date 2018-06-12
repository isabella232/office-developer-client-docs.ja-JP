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
description: 色の明度の値を返します。
ms.openlocfilehash: 9c9594aff0149a54d7faacdf8295e6c214c43348
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805810"
---
# <a name="lum-function"></a><span data-ttu-id="98b42-103">LUM 関数</span><span class="sxs-lookup"><span data-stu-id="98b42-103">LUM Function</span></span>

<span data-ttu-id="98b42-104">色の明度の値を返します。</span><span class="sxs-lookup"><span data-stu-id="98b42-104">Returns the value of a color's luminosity component.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="98b42-105">構文</span><span class="sxs-lookup"><span data-stu-id="98b42-105">Syntax</span></span>

<span data-ttu-id="98b42-106">明るさ (* **式** *)</span><span class="sxs-lookup"><span data-stu-id="98b42-106">LUM(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="98b42-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="98b42-107">Parameters</span></span>

|<span data-ttu-id="98b42-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="98b42-108">**Name**</span></span>|<span data-ttu-id="98b42-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="98b42-109">**Required/Optional**</span></span>|<span data-ttu-id="98b42-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="98b42-110">**Data Type**</span></span>|<span data-ttu-id="98b42-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="98b42-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="98b42-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="98b42-112">_expression_</span></span> <br/> |<span data-ttu-id="98b42-113">必須</span><span class="sxs-lookup"><span data-stu-id="98b42-113">Required</span></span>  <br/> |<span data-ttu-id="98b42-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="98b42-114">**Numeric**</span></span> <br/> |<span data-ttu-id="98b42-115">図面のカラー テーブルにある色のインデックス、またはカラー インデックスを含むセルに対する参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="98b42-115">The index of a color in the document's color table, or a reference to a cell that contains a color index.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="98b42-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="98b42-116">Return value</span></span>

<span data-ttu-id="98b42-117">数値</span><span class="sxs-lookup"><span data-stu-id="98b42-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="98b42-118">注釈</span><span class="sxs-lookup"><span data-stu-id="98b42-118">Remarks</span></span>

<span data-ttu-id="98b42-p101">戻り値は 0 ～ 240 の数値です。入力した引数が無効な場合は、0 を返します。</span><span class="sxs-lookup"><span data-stu-id="98b42-p101">The return value is a number in the range 0 to 240, inclusive. The function returns 0 for invalid input.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="98b42-121">例 1</span><span class="sxs-lookup"><span data-stu-id="98b42-121">Example 1</span></span>

<span data-ttu-id="98b42-122">明るさ (Sheet.4!FillForegnd)</span><span class="sxs-lookup"><span data-stu-id="98b42-122">LUM(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="98b42-123">Sheet.4 について、前景の塗りつぶしの色に関する明度を返します。</span><span class="sxs-lookup"><span data-stu-id="98b42-123">Returns the luminosity of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="98b42-124">例 2</span><span class="sxs-lookup"><span data-stu-id="98b42-124">Example 2</span></span>

<span data-ttu-id="98b42-125">LUM(6)</span><span class="sxs-lookup"><span data-stu-id="98b42-125">LUM(6)</span></span>
  
<span data-ttu-id="98b42-126">図面が既定の Visio カラー パレットを使用する場合、120 を返します。Visio カラー パレットでは、インデックス 6 はマゼンタを示します。</span><span class="sxs-lookup"><span data-stu-id="98b42-126">Returns 120 if the document uses the default Visio color palette, where magenta is the color at index 6.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="98b42-127">例 3</span><span class="sxs-lookup"><span data-stu-id="98b42-127">Example 3</span></span>

<span data-ttu-id="98b42-128">LUM(HSL(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="98b42-128">LUM(HSL(10, 20, 30))</span></span>
  
<span data-ttu-id="98b42-129">30 を返します。</span><span class="sxs-lookup"><span data-stu-id="98b42-129">Returns 30.</span></span>
  

