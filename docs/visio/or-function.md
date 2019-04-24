---
title: OR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251476
localization_priority: Normal
ms.assetid: 6c2154fa-4190-0699-61f7-f2bdf87173ec
description: パラメーターとして渡された論理式が true の場合は true (1) を返します。
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337213"
---
# <a name="or-function"></a><span data-ttu-id="c5c9f-103">OR 関数</span><span class="sxs-lookup"><span data-stu-id="c5c9f-103">OR Function</span></span>

<span data-ttu-id="c5c9f-104">パラメーターとして渡された論理式が true の場合は true (1) を返します。</span><span class="sxs-lookup"><span data-stu-id="c5c9f-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c5c9f-105">構文</span><span class="sxs-lookup"><span data-stu-id="c5c9f-105">Syntax</span></span>

<span data-ttu-id="c5c9f-106">OR (\* \* *logicalexpression1* \* *、* \* *logicalexpression2* \* \*,..., \* \* *logicalexpression n* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c5c9f-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c5c9f-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c5c9f-107">Parameters</span></span>

|<span data-ttu-id="c5c9f-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c5c9f-108">**Name**</span></span>|<span data-ttu-id="c5c9f-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c5c9f-109">**Required/Optional**</span></span>|<span data-ttu-id="c5c9f-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c5c9f-110">**Data Type**</span></span>|<span data-ttu-id="c5c9f-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c5c9f-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c5c9f-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="c5c9f-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="c5c9f-113">必須</span><span class="sxs-lookup"><span data-stu-id="c5c9f-113">Required</span></span>  <br/> |<span data-ttu-id="c5c9f-114">**String**</span><span class="sxs-lookup"><span data-stu-id="c5c9f-114">**String**</span></span> <br/> |<span data-ttu-id="c5c9f-115">真を評価する最初の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="c5c9f-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="c5c9f-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="c5c9f-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="c5c9f-117">必須</span><span class="sxs-lookup"><span data-stu-id="c5c9f-117">Required</span></span>  <br/> |<span data-ttu-id="c5c9f-118">**String**</span><span class="sxs-lookup"><span data-stu-id="c5c9f-118">**String**</span></span> <br/> |<span data-ttu-id="c5c9f-119">真を評価する 2 番目の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="c5c9f-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="c5c9f-120">_logical式 n_</span><span class="sxs-lookup"><span data-stu-id="c5c9f-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="c5c9f-121">必須</span><span class="sxs-lookup"><span data-stu-id="c5c9f-121">Required</span></span>  <br/> |<span data-ttu-id="c5c9f-122">**String**</span><span class="sxs-lookup"><span data-stu-id="c5c9f-122">**String**</span></span> <br/> |<span data-ttu-id="c5c9f-123">真を評価する n 番目の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="c5c9f-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c5c9f-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="c5c9f-124">Return value</span></span>

<span data-ttu-id="c5c9f-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="c5c9f-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c5c9f-126">解説</span><span class="sxs-lookup"><span data-stu-id="c5c9f-126">Remarks</span></span>

<span data-ttu-id="c5c9f-p101">いずれかの式がゼロ以外の値に評価される場合は、TRUE と見なされます。すべての論理式が FALSE または 0 の場合に、この関数は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="c5c9f-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="c5c9f-129">例</span><span class="sxs-lookup"><span data-stu-id="c5c9f-129">Example</span></span>

<span data-ttu-id="c5c9f-130">OR (Height \> 1、PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="c5c9f-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="c5c9f-131">どちらかの式が TRUE の場合、TRUE (1) を返します。</span><span class="sxs-lookup"><span data-stu-id="c5c9f-131">Returns TRUE (1) if either expression is TRUE.</span></span> <span data-ttu-id="c5c9f-132">両方の式が FALSE の場合にのみ、FALSE (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="c5c9f-132">Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

