---
title: GREEN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251434
localization_priority: Normal
ms.assetid: eccec432-32d3-15c2-06b3-dd02b6313d4c
description: 色の緑コンポーネントを返します。
ms.openlocfilehash: 0412e4519c2964b05d7663805d7773e8dc5deaab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438107"
---
# <a name="green-function"></a><span data-ttu-id="ebf7f-103">GREEN 関数</span><span class="sxs-lookup"><span data-stu-id="ebf7f-103">GREEN Function</span></span>

<span data-ttu-id="ebf7f-104">色の緑コンポーネントを返します。</span><span class="sxs-lookup"><span data-stu-id="ebf7f-104">Returns the green component of a color.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="ebf7f-105">構文</span><span class="sxs-lookup"><span data-stu-id="ebf7f-105">Syntax</span></span>

<span data-ttu-id="ebf7f-106">緑 (\* **式** \*)</span><span class="sxs-lookup"><span data-stu-id="ebf7f-106">GREEN(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="ebf7f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="ebf7f-107">Parameters</span></span>

|<span data-ttu-id="ebf7f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="ebf7f-108">**Name**</span></span>|<span data-ttu-id="ebf7f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="ebf7f-109">**Required/Optional**</span></span>|<span data-ttu-id="ebf7f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="ebf7f-110">**Data Type**</span></span>|<span data-ttu-id="ebf7f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="ebf7f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="ebf7f-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="ebf7f-112">_expression_</span></span> <br/> |<span data-ttu-id="ebf7f-113">必須</span><span class="sxs-lookup"><span data-stu-id="ebf7f-113">Required</span></span>  <br/> |<span data-ttu-id="ebf7f-114">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="ebf7f-114">**Varies**</span></span> <br/> |<span data-ttu-id="ebf7f-115">ドキュメントのカラーテーブルにある色のインデックス、ユーザー設定の色に解決される式 (RGB や HSL など)、またはカラーインデックスや色の結果を含むセルへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="ebf7f-115">An index of a color in the document's color table, an expression that resolves to a custom color (such as RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="ebf7f-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="ebf7f-116">Return value</span></span>

<span data-ttu-id="ebf7f-117">整数</span><span class="sxs-lookup"><span data-stu-id="ebf7f-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="ebf7f-118">注釈</span><span class="sxs-lookup"><span data-stu-id="ebf7f-118">Remarks</span></span>

<span data-ttu-id="ebf7f-119">戻り値は、0 ～ 255 の数値、またはインデックスを判別するセル参照になります。</span><span class="sxs-lookup"><span data-stu-id="ebf7f-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="ebf7f-120">*式*が無効な場合は、0 (黒) を返します。</span><span class="sxs-lookup"><span data-stu-id="ebf7f-120">If  *expression*  is invalid, it returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="ebf7f-121">例 1</span><span class="sxs-lookup"><span data-stu-id="ebf7f-121">Example 1</span></span>

<span data-ttu-id="ebf7f-122">緑 (Sheet. 4![fillforegnd]</span><span class="sxs-lookup"><span data-stu-id="ebf7f-122">GREEN(Sheet.4!FillForegnd)</span></span>
  
<span data-ttu-id="ebf7f-123">Sheet.4 について、前景の塗りつぶしの色に関する緑のコンポーネントを返します。</span><span class="sxs-lookup"><span data-stu-id="ebf7f-123">Returns the green component of Sheet.4's fill foreground color.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="ebf7f-124">例 2</span><span class="sxs-lookup"><span data-stu-id="ebf7f-124">Example 2</span></span>

<span data-ttu-id="ebf7f-125">緑 (11)</span><span class="sxs-lookup"><span data-stu-id="ebf7f-125">GREEN(11)</span></span>
  
<span data-ttu-id="ebf7f-126">図面で既定の Visio カラー パレットを使用する場合、128 を返します。Visio カラー パレットでは、インデックス 11 は濃い黄を示します。</span><span class="sxs-lookup"><span data-stu-id="ebf7f-126">Returns 128 if the document uses the default Visio color palette, where dark yellow is the color at index 11.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="ebf7f-127">例 3</span><span class="sxs-lookup"><span data-stu-id="ebf7f-127">Example 3</span></span>

<span data-ttu-id="ebf7f-128">GREEN(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="ebf7f-128">GREEN(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="ebf7f-129">20 を返します。</span><span class="sxs-lookup"><span data-stu-id="ebf7f-129">Returns 20.</span></span>
  

