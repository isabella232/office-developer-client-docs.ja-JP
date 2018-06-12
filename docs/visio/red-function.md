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
description: 色の赤の要素を返します。
ms.openlocfilehash: 801ebb64564df81f72c41cb720fe53f0f1b4c10d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806146"
---
# <a name="red-function"></a><span data-ttu-id="b0e07-103">RED 関数</span><span class="sxs-lookup"><span data-stu-id="b0e07-103">RED Function</span></span>

<span data-ttu-id="b0e07-104">色の赤の要素を返します。</span><span class="sxs-lookup"><span data-stu-id="b0e07-104">Returns the red component of a color.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b0e07-105">構文</span><span class="sxs-lookup"><span data-stu-id="b0e07-105">Syntax</span></span>

<span data-ttu-id="b0e07-106">赤 (* **式** *)</span><span class="sxs-lookup"><span data-stu-id="b0e07-106">RED(** *expression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b0e07-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="b0e07-107">Parameters</span></span>

|<span data-ttu-id="b0e07-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="b0e07-108">**Name**</span></span>|<span data-ttu-id="b0e07-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b0e07-109">**Required/Optional**</span></span>|<span data-ttu-id="b0e07-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b0e07-110">**Data Type**</span></span>|<span data-ttu-id="b0e07-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b0e07-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b0e07-112">_expression_</span><span class="sxs-lookup"><span data-stu-id="b0e07-112">_expression_</span></span> <br/> |<span data-ttu-id="b0e07-113">必須</span><span class="sxs-lookup"><span data-stu-id="b0e07-113">Required</span></span>  <br/> |<span data-ttu-id="b0e07-114">**によって異なります**</span><span class="sxs-lookup"><span data-stu-id="b0e07-114">**Varies**</span></span> <br/> |<span data-ttu-id="b0e07-115">引数として、図面のカラー テーブルにある色のインデックス、ユーザー設定の色を返す式 (RGB や HSL など)、またはカラー インデックスや色の結果を含むセルへの参照を指定します。</span><span class="sxs-lookup"><span data-stu-id="b0e07-115">An index of a color in the document's color table, an expression that resolves to a custom color (like RGB or HSL), or a reference to a cell that contains a color index or color result.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="b0e07-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="b0e07-116">Return value</span></span>

<span data-ttu-id="b0e07-117">数値</span><span class="sxs-lookup"><span data-stu-id="b0e07-117">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b0e07-118">注釈</span><span class="sxs-lookup"><span data-stu-id="b0e07-118">Remarks</span></span>

<span data-ttu-id="b0e07-119">戻り値は、0 ~ 255 の範囲、範囲内の数値、またはインデックスを判別するセル参照です。</span><span class="sxs-lookup"><span data-stu-id="b0e07-119">The return value is a number in the range 0 to 255, inclusive, or a cell reference that resolves to an index.</span></span> <span data-ttu-id="b0e07-120">_式_が有効でない場合、この関数は 0 (黒) を返します。</span><span class="sxs-lookup"><span data-stu-id="b0e07-120">If  _expression_ is invalid, this function returns 0 (black).</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="b0e07-121">例 1</span><span class="sxs-lookup"><span data-stu-id="b0e07-121">Example 1</span></span>

<span data-ttu-id="b0e07-122">RED(22)</span><span class="sxs-lookup"><span data-stu-id="b0e07-122">RED(22)</span></span>
  
<span data-ttu-id="b0e07-123">図面が既定の Microsoft Office Visio カラー パレットを使用する場合、51 を返します。Visio カラー パレットでは、インデックス 22 は濃い灰色を示します。</span><span class="sxs-lookup"><span data-stu-id="b0e07-123">Returns 51 if the document uses the default Microsoft Office Visio color palette, where dark gray is the color at index 22.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="b0e07-124">例 2</span><span class="sxs-lookup"><span data-stu-id="b0e07-124">Example 2</span></span>

<span data-ttu-id="b0e07-125">RED(Char.Color)</span><span class="sxs-lookup"><span data-stu-id="b0e07-125">RED(Char.Color)</span></span>
  
<span data-ttu-id="b0e07-126">現在のフォントの色について、赤のコンポーネントの値を返します。</span><span class="sxs-lookup"><span data-stu-id="b0e07-126">Returns the value of the red component of the current font color.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="b0e07-127">例 3</span><span class="sxs-lookup"><span data-stu-id="b0e07-127">Example 3</span></span>

<span data-ttu-id="b0e07-128">RED(RGB(10, 20, 30))</span><span class="sxs-lookup"><span data-stu-id="b0e07-128">RED(RGB(10, 20, 30))</span></span>
  
<span data-ttu-id="b0e07-129">10 を返します。</span><span class="sxs-lookup"><span data-stu-id="b0e07-129">Returns 10.</span></span>
  

