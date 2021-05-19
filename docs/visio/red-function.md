---
title: RED 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251487
localization_priority: Normal
ms.assetid: a95fd86d-ebc1-66b6-e7d9-9c8ea84d23ab
description: 色の赤いコンポーネントを返します。
ms.openlocfilehash: e8c6115ac0441b25ce8333485828e8ef0f615459
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415524"
---
# <a name="red-function"></a><span data-ttu-id="d0343-103">RED 関数</span><span class="sxs-lookup"><span data-stu-id="d0343-103">RED Function</span></span>

<span data-ttu-id="d0343-104">色の赤いコンポーネントを返します。</span><span class="sxs-lookup"><span data-stu-id="d0343-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d0343-105">構文</span><span class="sxs-lookup"><span data-stu-id="d0343-105">Syntax</span></span>

<span data-ttu-id="d0343-106">RED(\*\* *式* \*\* )</span><span class="sxs-lookup"><span data-stu-id="d0343-106">RED(\*\* *expression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d0343-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d0343-107">Parameters</span></span>

|<span data-ttu-id="d0343-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d0343-108">**Name**</span></span>|<span data-ttu-id="d0343-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d0343-109">**Required/Optional**</span></span>|<span data-ttu-id="d0343-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d0343-110">**Data Type**</span></span>|<span data-ttu-id="d0343-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d0343-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d0343-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="d0343-112">_expression_</span></span> <br/> |<span data-ttu-id="d0343-113">必須</span><span class="sxs-lookup"><span data-stu-id="d0343-113">Required</span></span>  <br/> |<span data-ttu-id="d0343-114">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="d0343-114">**Varies**</span></span> <br/> |<span data-ttu-id="d0343-115">引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="d0343-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d0343-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="d0343-116">Return value</span></span>

<span data-ttu-id="d0343-117">番号</span><span class="sxs-lookup"><span data-stu-id="d0343-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d0343-118">注釈</span><span class="sxs-lookup"><span data-stu-id="d0343-118">Remarks</span></span>

<span data-ttu-id="d0343-119">戻り値は、0 ～ 255 の数値、またはインデックスを判別するセル参照になります。</span><span class="sxs-lookup"><span data-stu-id="d0343-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="d0343-120">式  _が_ 無効な場合、この関数は 0 (黒) を返します。</span><span class="sxs-lookup"><span data-stu-id="d0343-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="d0343-121">例 1</span><span class="sxs-lookup"><span data-stu-id="d0343-121">Example 1</span></span>

<span data-ttu-id="d0343-122">RED(22)</span><span class="sxs-lookup"><span data-stu-id="d0343-122">RED(22)</span></span>
  
<span data-ttu-id="d0343-123">図面が既定の Microsoft Office Visio カラー パレットを使用する場合、51 を返します。Visio カラー パレットでは、インデックス 22 は濃い灰色を示します。</span><span class="sxs-lookup"><span data-stu-id="d0343-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d0343-124">例 2</span><span class="sxs-lookup"><span data-stu-id="d0343-124">Example 2</span></span>

<span data-ttu-id="d0343-125">RED(Char.Color)</span><span class="sxs-lookup"><span data-stu-id="d0343-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="d0343-126">現在のフォントの色について、赤のコンポーネントの値を返します。</span><span class="sxs-lookup"><span data-stu-id="d0343-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="d0343-127">例 3</span><span class="sxs-lookup"><span data-stu-id="d0343-127">Example 3</span></span>

<span data-ttu-id="d0343-128">RED(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="d0343-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="d0343-129">10 を返します。</span><span class="sxs-lookup"><span data-stu-id="d0343-129">Returns 10.</span></span>
  

