---
title: USERUI 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251511
localization_priority: Normal
ms.assetid: c01dd938-677c-b2ba-8f56-4638e7e988fd
description: state の値に応じて、2つの式のいずれかを評価します。
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331326"
---
# <a name="userui-function"></a><span data-ttu-id="910bc-103">USERUI 関数</span><span class="sxs-lookup"><span data-stu-id="910bc-103">USERUI Function</span></span>

<span data-ttu-id="910bc-104">_state_の値に応じて、2つの式のいずれかを評価します。</span><span class="sxs-lookup"><span data-stu-id="910bc-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="910bc-105">構文</span><span class="sxs-lookup"><span data-stu-id="910bc-105">Syntax</span></span>

<span data-ttu-id="910bc-106">userui (\* \* *state* \* \*, \* \* *defaultexpression* \* \*, \* \* *userui* \* \*)</span><span class="sxs-lookup"><span data-stu-id="910bc-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="910bc-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="910bc-107">Parameters</span></span>

|<span data-ttu-id="910bc-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="910bc-108">**Name**</span></span>|<span data-ttu-id="910bc-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="910bc-109">**Required/Optional**</span></span>|<span data-ttu-id="910bc-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="910bc-110">**Data Type**</span></span>|<span data-ttu-id="910bc-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="910bc-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="910bc-112">_state_</span><span class="sxs-lookup"><span data-stu-id="910bc-112">_state_</span></span> <br/> |<span data-ttu-id="910bc-113">必須</span><span class="sxs-lookup"><span data-stu-id="910bc-113">Required</span></span>  <br/> |<span data-ttu-id="910bc-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="910bc-114">**Boolean**</span></span> <br/> |<span data-ttu-id="910bc-115">評価する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="910bc-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="910bc-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="910bc-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="910bc-117">必須</span><span class="sxs-lookup"><span data-stu-id="910bc-117">Required</span></span>  <br/> |<span data-ttu-id="910bc-118">**String**</span><span class="sxs-lookup"><span data-stu-id="910bc-118">**String**</span></span> <br/> |<span data-ttu-id="910bc-119">既定の式を指定します。</span><span class="sxs-lookup"><span data-stu-id="910bc-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="910bc-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="910bc-120">_userexpression_</span></span> <br/> |<span data-ttu-id="910bc-121">必須</span><span class="sxs-lookup"><span data-stu-id="910bc-121">Required</span></span>  <br/> |<span data-ttu-id="910bc-122">**String**</span><span class="sxs-lookup"><span data-stu-id="910bc-122">**String**</span></span> <br/> |<span data-ttu-id="910bc-123">ユーザーによって指定された式。</span><span class="sxs-lookup"><span data-stu-id="910bc-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="910bc-124">解説</span><span class="sxs-lookup"><span data-stu-id="910bc-124">Remarks</span></span>

<span data-ttu-id="910bc-125">_state_が0の場合、userui 関数は_defaultexpression_を評価します。</span><span class="sxs-lookup"><span data-stu-id="910bc-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="910bc-126">_state_が1の場合は、 _userexpression_を評価します。</span><span class="sxs-lookup"><span data-stu-id="910bc-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="910bc-127">例</span><span class="sxs-lookup"><span data-stu-id="910bc-127">Example</span></span>

<span data-ttu-id="910bc-128">userui (1, if (幅\>6in, 6in, width), 幅\*0.75)</span><span class="sxs-lookup"><span data-stu-id="910bc-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="910bc-129">式の幅\*075 を評価し、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="910bc-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

