---
title: ROUND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: Numberofdigits によって表される有効桁数に四捨五入します。
ms.openlocfilehash: 2457bdf6b46a2bb44b203497f02cc9b2ff034847
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/21/2018
ms.locfileid: "19806260"
---
# <a name="round-function-visioshapesheet"></a><span data-ttu-id="df1c9-103">ROUND 関数 (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="df1c9-103">ROUND Function (VisioShapeSheet)</span></span>

<span data-ttu-id="df1c9-104">*Numberofdigits*によって表される有効桁数に四捨五入します。</span><span class="sxs-lookup"><span data-stu-id="df1c9-104">Rounds a number to the precision represented by  *numberofdigits*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="df1c9-105">構文</span><span class="sxs-lookup"><span data-stu-id="df1c9-105">Syntax</span></span>

<span data-ttu-id="df1c9-106">ラウンド (* **番号** *、* * *numberofdigits* * *)</span><span class="sxs-lookup"><span data-stu-id="df1c9-106">ROUND(** *number* **, ** *numberofdigits* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="df1c9-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="df1c9-107">Parameters</span></span>

|<span data-ttu-id="df1c9-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="df1c9-108">**Name**</span></span>|<span data-ttu-id="df1c9-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="df1c9-109">**Required/Optional**</span></span>|<span data-ttu-id="df1c9-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="df1c9-110">**Data Type**</span></span>|<span data-ttu-id="df1c9-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="df1c9-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="df1c9-112">_number_</span><span class="sxs-lookup"><span data-stu-id="df1c9-112">_number_</span></span> <br/> |<span data-ttu-id="df1c9-113">必須</span><span class="sxs-lookup"><span data-stu-id="df1c9-113">Required</span></span>  <br/> |<span data-ttu-id="df1c9-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="df1c9-114">**Number**</span></span> <br/> |<span data-ttu-id="df1c9-115">四捨五入の対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="df1c9-115">The number to round off.</span></span>  <br/> |
| <span data-ttu-id="df1c9-116">_numberofdigits_</span><span class="sxs-lookup"><span data-stu-id="df1c9-116">_numberofdigits_</span></span> <br/> |<span data-ttu-id="df1c9-117">必須</span><span class="sxs-lookup"><span data-stu-id="df1c9-117">Required</span></span>  <br/> |<span data-ttu-id="df1c9-118">**番号**</span><span class="sxs-lookup"><span data-stu-id="df1c9-118">**Number**</span></span> <br/> |<span data-ttu-id="df1c9-119">精度の小数点以下桁数を指定します。</span><span class="sxs-lookup"><span data-stu-id="df1c9-119">The number of decimal places of precision.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df1c9-120">注釈</span><span class="sxs-lookup"><span data-stu-id="df1c9-120">Remarks</span></span>

<span data-ttu-id="df1c9-121">_Numberofdigits_が 0 より大きい場合は、小数点の右側に_numberofdigits_で_数値_が丸められます。</span><span class="sxs-lookup"><span data-stu-id="df1c9-121">If  _numberofdigits_ is greater than 0,  _number_ is rounded by  _numberofdigits_ to the right of the decimal.</span></span> <span data-ttu-id="df1c9-122">_Numberofdigits_が 0 の場合は、_数値_は整数に丸められます。</span><span class="sxs-lookup"><span data-stu-id="df1c9-122">If  _numberofdigits_ is 0,  _number_ is rounded to an integer.</span></span> <span data-ttu-id="df1c9-123">_Numberofdigits_が 0 より小さい場合は、小数点の左側に_numberofdigits_で_数値_が丸められます。</span><span class="sxs-lookup"><span data-stu-id="df1c9-123">If  _numberofdigits_ is less than 0,  _number_ is rounded by  _numberofdigits_ to the left of the decimal.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="df1c9-124">例 1</span><span class="sxs-lookup"><span data-stu-id="df1c9-124">Example 1</span></span>

<span data-ttu-id="df1c9-125">ROUND(123.654,2)</span><span class="sxs-lookup"><span data-stu-id="df1c9-125">ROUND(123.654,2)</span></span>
  
<span data-ttu-id="df1c9-126">123.65 を返します。</span><span class="sxs-lookup"><span data-stu-id="df1c9-126">Returns 123.65.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="df1c9-127">例 2</span><span class="sxs-lookup"><span data-stu-id="df1c9-127">Example 2</span></span>

<span data-ttu-id="df1c9-128">ROUND(123.654,0)</span><span class="sxs-lookup"><span data-stu-id="df1c9-128">ROUND(123.654,0)</span></span>
  
<span data-ttu-id="df1c9-129">124 を返します。</span><span class="sxs-lookup"><span data-stu-id="df1c9-129">Returns 124.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="df1c9-130">例 3</span><span class="sxs-lookup"><span data-stu-id="df1c9-130">Example 3</span></span>

<span data-ttu-id="df1c9-131">ROUND(123.654,-1)</span><span class="sxs-lookup"><span data-stu-id="df1c9-131">ROUND(123.654,-1)</span></span>
  
<span data-ttu-id="df1c9-132">120 を返します。</span><span class="sxs-lookup"><span data-stu-id="df1c9-132">Returns 120.</span></span>
  

