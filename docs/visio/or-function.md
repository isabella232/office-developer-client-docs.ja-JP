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
description: パラメーターとして渡された論理式のいずれかが TRUE である場合は、TRUE (1) を返します。
ms.openlocfilehash: 14646f553e76c8c395fdbde8762daf75114f9480
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805948"
---
# <a name="or-function"></a><span data-ttu-id="d8af4-103">OR 関数</span><span class="sxs-lookup"><span data-stu-id="d8af4-103">OR Function</span></span>

<span data-ttu-id="d8af4-104">パラメーターとして渡された論理式のいずれかが TRUE である場合は、TRUE (1) を返します。</span><span class="sxs-lookup"><span data-stu-id="d8af4-104">Returns TRUE (1) if any of the logical expressions passed as parameters are TRUE.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d8af4-105">構文</span><span class="sxs-lookup"><span data-stu-id="d8af4-105">Syntax</span></span>

<span data-ttu-id="d8af4-106">または (* * *logicalexpression1* * *、* * *logicalexpression2* * *、* * *logicalexpressionN* * *)</span><span class="sxs-lookup"><span data-stu-id="d8af4-106">OR(** *logicalexpression1* **, ** *logicalexpression2* **,..., ** *logicalexpressionN* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d8af4-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="d8af4-107">Parameters</span></span>

|<span data-ttu-id="d8af4-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d8af4-108">**Name**</span></span>|<span data-ttu-id="d8af4-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d8af4-109">**Required/Optional**</span></span>|<span data-ttu-id="d8af4-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d8af4-110">**Data Type**</span></span>|<span data-ttu-id="d8af4-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d8af4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d8af4-112">_logicalexpression1_</span><span class="sxs-lookup"><span data-stu-id="d8af4-112">_logicalexpression1_</span></span> <br/> |<span data-ttu-id="d8af4-113">必須</span><span class="sxs-lookup"><span data-stu-id="d8af4-113">Required</span></span>  <br/> |<span data-ttu-id="d8af4-114">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="d8af4-114">**String**</span></span> <br/> |<span data-ttu-id="d8af4-115">真を評価する最初の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8af4-115">The first expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="d8af4-116">_logicalexpression2_</span><span class="sxs-lookup"><span data-stu-id="d8af4-116">_logicalexpression2_</span></span> <br/> |<span data-ttu-id="d8af4-117">必須</span><span class="sxs-lookup"><span data-stu-id="d8af4-117">Required</span></span>  <br/> |<span data-ttu-id="d8af4-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="d8af4-118">**String**</span></span> <br/> |<span data-ttu-id="d8af4-119">真を評価する 2 番目の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8af4-119">The second expression whose truth you want to evaluate.</span></span>  <br/> |
| <span data-ttu-id="d8af4-120">_logicalexpressionN_</span><span class="sxs-lookup"><span data-stu-id="d8af4-120">_logicalexpressionN_</span></span> <br/> |<span data-ttu-id="d8af4-121">必須</span><span class="sxs-lookup"><span data-stu-id="d8af4-121">Required</span></span>  <br/> |<span data-ttu-id="d8af4-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="d8af4-122">**String**</span></span> <br/> |<span data-ttu-id="d8af4-123">真を評価する n 番目の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="d8af4-123">The Nth expression whose truth you want to evaluate.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d8af4-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="d8af4-124">Return value</span></span>

<span data-ttu-id="d8af4-125">ブール型 (Boolean)</span><span class="sxs-lookup"><span data-stu-id="d8af4-125">Boolean</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d8af4-126">注釈</span><span class="sxs-lookup"><span data-stu-id="d8af4-126">Remarks</span></span>

<span data-ttu-id="d8af4-p101">いずれかの式がゼロ以外の値に評価される場合は、TRUE と見なされます。すべての論理式が FALSE または 0 の場合に、この関数は FALSE を返します。</span><span class="sxs-lookup"><span data-stu-id="d8af4-p101">Any expression that evaluates to a non-zero value is considered TRUE. If all of the logical expressions are FALSE or equal 0, this function returns FALSE.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d8af4-129">例</span><span class="sxs-lookup"><span data-stu-id="d8af4-129">Example</span></span>

<span data-ttu-id="d8af4-130">または (高さ\>1 の場合、[pinx] \> 1)</span><span class="sxs-lookup"><span data-stu-id="d8af4-130">OR(Height \> 1,PinX \> 1)</span></span> 
  
<span data-ttu-id="d8af4-p102">どちらかの式が TRUE の場合、TRUE (1) を返します。両方の式が FALSE の場合にのみ、FALSE (0) を返します。</span><span class="sxs-lookup"><span data-stu-id="d8af4-p102">Returns TRUE (1) if either expression is TRUE. Returns FALSE (0) only if both expressions are FALSE.</span></span> 
  

