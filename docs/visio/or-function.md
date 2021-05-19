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
description: パラメーターとして渡される論理式が TRUE の場合は、TRUE (1) を返します。
ms.openlocfilehash: 175a1c72f5109caca786b823966f07836f4737f0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433508"
---
# <a name="or-function"></a><span data-ttu-id="a13ec-103">OR 関数</span><span class="sxs-lookup"><span data-stu-id="a13ec-103">OR Function</span></span>

<span data-ttu-id="a13ec-104">パラメーターとして渡される論理式が TRUE の場合は、TRUE (1) を返します。</span><span class="sxs-lookup"><span data-stu-id="a13ec-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a13ec-105">構文</span><span class="sxs-lookup"><span data-stu-id="a13ec-105">Syntax</span></span>

<span data-ttu-id="a13ec-106">OR(\*\* *logicalexpression1* \*\*, \*\* \*logicalexpression2 \**,...,* \*\* *logicalexpressionN* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a13ec-106">OR(\*\* *logicalexpression1* \*\*, \*\* *logicalexpression2* \*\*,..., \*\* *logicalexpressionN* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a13ec-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a13ec-107">Parameters</span></span>

|<span data-ttu-id="a13ec-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a13ec-108">**Name**</span></span>|<span data-ttu-id="a13ec-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a13ec-109">**Required/Optional**</span></span>|<span data-ttu-id="a13ec-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a13ec-110">**Data Type**</span></span>|<span data-ttu-id="a13ec-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a13ec-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a13ec-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="a13ec-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="a13ec-113">必須</span><span class="sxs-lookup"><span data-stu-id="a13ec-113">Required</span></span>  <br/> |<span data-ttu-id="a13ec-114">**String**</span><span class="sxs-lookup"><span data-stu-id="a13ec-114">**String**</span></span> <br/> |<span data-ttu-id="a13ec-115">真を評価する最初の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a13ec-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a13ec-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="a13ec-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="a13ec-117">必須</span><span class="sxs-lookup"><span data-stu-id="a13ec-117">Required</span></span>  <br/> |<span data-ttu-id="a13ec-118">**String**</span><span class="sxs-lookup"><span data-stu-id="a13ec-118">**String**</span></span> <br/> |<span data-ttu-id="a13ec-119">真を評価する 2 番目の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a13ec-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="a13ec-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="a13ec-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="a13ec-121">必須</span><span class="sxs-lookup"><span data-stu-id="a13ec-121">Required</span></span>  <br/> |<span data-ttu-id="a13ec-122">**String**</span><span class="sxs-lookup"><span data-stu-id="a13ec-122">**String**</span></span> <br/> |<span data-ttu-id="a13ec-123">真を評価する n 番目の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="a13ec-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a13ec-124">戻り値</span><span class="sxs-lookup"><span data-stu-id="a13ec-124">Return value</span></span>

<span data-ttu-id="a13ec-125">Boolean</span><span class="sxs-lookup"><span data-stu-id="a13ec-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a13ec-126">注釈</span><span class="sxs-lookup"><span data-stu-id="a13ec-126">Remarks</span></span>

<span data-ttu-id="a13ec-p101">いずれかの式がゼロ以外の値に評価される場合は、TRUE と見なされます。すべての論理式が FALSE または 0 の場合に、この関数は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="a13ec-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="a13ec-129">例</span><span class="sxs-lookup"><span data-stu-id="a13ec-129">Example</span></span>

<span data-ttu-id="a13ec-130">OR(Height \> 1,PinX \> 1)</span><span class="sxs-lookup"><span data-stu-id="a13ec-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="a13ec-p102">どちらかの式が TRUE の場合、TRUE (1) を返します。両方の式が FALSE の場合にのみ、FALSE (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="a13ec-p102">Returns TRUE (1) if either expression is TRUE. Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

