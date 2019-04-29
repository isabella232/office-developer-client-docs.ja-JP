---
title: IF 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251442
localization_priority: Normal
ms.assetid: 66771ad3-0fb3-68ff-81da-d1162d37c05a
description: logicalexpression が true の場合は、valueiftrue を返します。 それ以外の場合は、valueiffalse を返します。
ms.openlocfilehash: 8780bd3dd5ded1a950a5bf3f79333687f3b6843c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405472"
---
# <a name="if-function"></a><span data-ttu-id="f5954-104">IF 関数</span><span class="sxs-lookup"><span data-stu-id="f5954-104">IF Function</span></span>

<span data-ttu-id="f5954-105">_logicalexpression_が true の場合は、 _valueiftrue_を返します。</span><span class="sxs-lookup"><span data-stu-id="f5954-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="f5954-106">それ以外の場合は、 _valueiffalse_を返します。</span><span class="sxs-lookup"><span data-stu-id="f5954-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="f5954-107">構文</span><span class="sxs-lookup"><span data-stu-id="f5954-107">Syntax</span></span>

<span data-ttu-id="f5954-108">IF (\* \* *logicalexpression* \* \*, \* \* *valueiftrue* \* \*, \* \* *valueiffalse* \* \*)</span><span class="sxs-lookup"><span data-stu-id="f5954-108">IF(\*\* *logicalexpression* \*\*, \*\* *valueiftrue* \*\*, \*\* *valueiffalse* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f5954-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="f5954-109">Parameters</span></span>

|<span data-ttu-id="f5954-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="f5954-110">**Name**</span></span>|<span data-ttu-id="f5954-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f5954-111">**Required/Optional**</span></span>|<span data-ttu-id="f5954-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f5954-112">**Data Type**</span></span>|<span data-ttu-id="f5954-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="f5954-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f5954-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="f5954-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="f5954-115">必須</span><span class="sxs-lookup"><span data-stu-id="f5954-115">Required</span></span>  <br/> |<span data-ttu-id="f5954-116">**String**</span><span class="sxs-lookup"><span data-stu-id="f5954-116">**String**</span></span> <br/> |<span data-ttu-id="f5954-117">評価する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="f5954-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="f5954-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="f5954-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="f5954-119">必須</span><span class="sxs-lookup"><span data-stu-id="f5954-119">Required</span></span>  <br/> |<span data-ttu-id="f5954-120">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="f5954-120">**Varies**</span></span> <br/> |<span data-ttu-id="f5954-121">_logicalexpression_が true の場合に返す値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f5954-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="f5954-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="f5954-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="f5954-123">必須</span><span class="sxs-lookup"><span data-stu-id="f5954-123">Required</span></span>  <br/> |<span data-ttu-id="f5954-124">**さまざま**</span><span class="sxs-lookup"><span data-stu-id="f5954-124">**Varies**</span></span> <br/> | <span data-ttu-id="f5954-125">_logicalexpression_が false の場合に返す値を指定します。</span><span class="sxs-lookup"><span data-stu-id="f5954-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f5954-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="f5954-126">Return value</span></span>

<span data-ttu-id="f5954-127">さまざま</span><span class="sxs-lookup"><span data-stu-id="f5954-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="f5954-128">例</span><span class="sxs-lookup"><span data-stu-id="f5954-128">Example</span></span>

<span data-ttu-id="f5954-129">IF (Height \> 1.25 in, 5, 7)</span><span class="sxs-lookup"><span data-stu-id="f5954-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="f5954-130">図形の高さが 1.25 インチを超える場合は、5 を返します。</span><span class="sxs-lookup"><span data-stu-id="f5954-130">Returns 5 if the shape's height is greater than 1.25 inches.</span></span> <span data-ttu-id="f5954-131">図形の高さが 1.25 インチ以下の場合は、7 を返します。</span><span class="sxs-lookup"><span data-stu-id="f5954-131">Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

