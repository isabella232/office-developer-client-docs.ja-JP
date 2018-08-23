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
description: Logicalexpression が TRUE の場合に、valueiftrue を返します。 Valueiffalse を返します。
ms.openlocfilehash: 55938e8bd78c02badb98f90665c5c26cdd70f3b7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805564"
---
# <a name="if-function"></a><span data-ttu-id="721eb-104">IF 関数</span><span class="sxs-lookup"><span data-stu-id="721eb-104">IF Function</span></span>

<span data-ttu-id="721eb-105">_Logicalexpression_が TRUE の場合に、 _valueiftrue_を返します。</span><span class="sxs-lookup"><span data-stu-id="721eb-105">Returns  _valueiftrue_ if  _logicalexpression_ is TRUE.</span></span> <span data-ttu-id="721eb-106">_Valueiffalse_を返します。</span><span class="sxs-lookup"><span data-stu-id="721eb-106">Otherwise, it returns  _valueiffalse_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="721eb-107">構文</span><span class="sxs-lookup"><span data-stu-id="721eb-107">Syntax</span></span>

<span data-ttu-id="721eb-108">IF (* * *logicalexpression* * *、* * *valueiftrue* * *、* * *valueiffalse* * *)</span><span class="sxs-lookup"><span data-stu-id="721eb-108">IF(** *logicalexpression* **, ** *valueiftrue* **, ** *valueiffalse* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="721eb-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="721eb-109">Parameters</span></span>

|<span data-ttu-id="721eb-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="721eb-110">**Name**</span></span>|<span data-ttu-id="721eb-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="721eb-111">**Required/Optional**</span></span>|<span data-ttu-id="721eb-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="721eb-112">**Data Type**</span></span>|<span data-ttu-id="721eb-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="721eb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="721eb-114">_logicalexpression_</span><span class="sxs-lookup"><span data-stu-id="721eb-114">_logicalexpression_</span></span> <br/> |<span data-ttu-id="721eb-115">必須</span><span class="sxs-lookup"><span data-stu-id="721eb-115">Required</span></span>  <br/> |<span data-ttu-id="721eb-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="721eb-116">**String**</span></span> <br/> |<span data-ttu-id="721eb-117">評価する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="721eb-117">Expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="721eb-118">_valueiftrue_</span><span class="sxs-lookup"><span data-stu-id="721eb-118">_valueiftrue_</span></span> <br/> |<span data-ttu-id="721eb-119">必須</span><span class="sxs-lookup"><span data-stu-id="721eb-119">Required</span></span>  <br/> |<span data-ttu-id="721eb-120">**多様**</span><span class="sxs-lookup"><span data-stu-id="721eb-120">**Varies**</span></span> <br/> |<span data-ttu-id="721eb-121">_Logicalexpression_が true のかどうかに返す値です。</span><span class="sxs-lookup"><span data-stu-id="721eb-121">Value to return if  _logicalexpression_ is true.</span></span>  <br/> |
| <span data-ttu-id="721eb-122">_valueiffalse_</span><span class="sxs-lookup"><span data-stu-id="721eb-122">_valueiffalse_</span></span> <br/> |<span data-ttu-id="721eb-123">必須</span><span class="sxs-lookup"><span data-stu-id="721eb-123">Required</span></span>  <br/> |<span data-ttu-id="721eb-124">**多様**</span><span class="sxs-lookup"><span data-stu-id="721eb-124">**Varies**</span></span> <br/> | <span data-ttu-id="721eb-125">_Logicalexpression_が false のかどうかに返す値です。</span><span class="sxs-lookup"><span data-stu-id="721eb-125">Value to return if  _logicalexpression_ is false.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="721eb-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="721eb-126">Return value</span></span>

<span data-ttu-id="721eb-127">可変値</span><span class="sxs-lookup"><span data-stu-id="721eb-127">Varies</span></span>
  
## <a name="example"></a><span data-ttu-id="721eb-128">例</span><span class="sxs-lookup"><span data-stu-id="721eb-128">Example</span></span>

<span data-ttu-id="721eb-129">IF (高さ\>1.25 で、5、7)</span><span class="sxs-lookup"><span data-stu-id="721eb-129">IF(Height \> 1.25 in,5,7)</span></span>
  
<span data-ttu-id="721eb-p103">図形の高さが 1.25 インチを超える場合は、5 を返します。図形の高さが 1.25 インチ以下の場合は、7 を返します。</span><span class="sxs-lookup"><span data-stu-id="721eb-p103">Returns 5 if the shape's height is greater than 1.25 inches. Returns 7 if the shape's height is less than or equal to 1.25 inches.</span></span>
  

