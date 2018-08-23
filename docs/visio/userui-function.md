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
description: 状態の値に応じて、2 つの式のいずれかを評価します。
ms.openlocfilehash: 2cfdf23986a06dcc109106bd50a1a38e5af91313
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806746"
---
# <a name="userui-function"></a><span data-ttu-id="eee74-103">USERUI 関数</span><span class="sxs-lookup"><span data-stu-id="eee74-103">USERUI Function</span></span>

<span data-ttu-id="eee74-104">_状態_の値に応じて、2 つの式のいずれかを評価します。</span><span class="sxs-lookup"><span data-stu-id="eee74-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eee74-105">構文</span><span class="sxs-lookup"><span data-stu-id="eee74-105">Syntax</span></span>

<span data-ttu-id="eee74-106">USERUI (* **状態** *、* * *defaultexpression* * *、* * *userexpression* * *)</span><span class="sxs-lookup"><span data-stu-id="eee74-106">USERUI(** *state* **, ** *defaultexpression* **, ** *userexpression* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eee74-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eee74-107">Parameters</span></span>

|<span data-ttu-id="eee74-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="eee74-108">**Name**</span></span>|<span data-ttu-id="eee74-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="eee74-109">**Required/Optional**</span></span>|<span data-ttu-id="eee74-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="eee74-110">**Data Type**</span></span>|<span data-ttu-id="eee74-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="eee74-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eee74-112">_state_</span><span class="sxs-lookup"><span data-stu-id="eee74-112">_state_</span></span> <br/> |<span data-ttu-id="eee74-113">必須</span><span class="sxs-lookup"><span data-stu-id="eee74-113">Required</span></span>  <br/> |<span data-ttu-id="eee74-114">**ブール型 (Boolean)**</span><span class="sxs-lookup"><span data-stu-id="eee74-114">**Boolean**</span></span> <br/> |<span data-ttu-id="eee74-115">評価する式を指定します。</span><span class="sxs-lookup"><span data-stu-id="eee74-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="eee74-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="eee74-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="eee74-117">必須</span><span class="sxs-lookup"><span data-stu-id="eee74-117">Required</span></span>  <br/> |<span data-ttu-id="eee74-118">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="eee74-118">**String**</span></span> <br/> |<span data-ttu-id="eee74-119">既定の式。</span><span class="sxs-lookup"><span data-stu-id="eee74-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="eee74-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="eee74-120">_userexpression_</span></span> <br/> |<span data-ttu-id="eee74-121">必須</span><span class="sxs-lookup"><span data-stu-id="eee74-121">Required</span></span>  <br/> |<span data-ttu-id="eee74-122">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="eee74-122">**String**</span></span> <br/> |<span data-ttu-id="eee74-123">ユーザーによって指定された式を指定します。</span><span class="sxs-lookup"><span data-stu-id="eee74-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="eee74-124">注釈</span><span class="sxs-lookup"><span data-stu-id="eee74-124">Remarks</span></span>

<span data-ttu-id="eee74-125">_状態_が 0 の場合、USERUI 関数は_defaultexpression_を評価します。</span><span class="sxs-lookup"><span data-stu-id="eee74-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="eee74-126">_状態_が 1 の場合は、 _userexpression_を評価します。</span><span class="sxs-lookup"><span data-stu-id="eee74-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="eee74-127">例</span><span class="sxs-lookup"><span data-stu-id="eee74-127">Example</span></span>

<span data-ttu-id="eee74-128">USERUI (1, 場合 (幅\>6 インチ、6 インチ、幅)、幅\*0.75)</span><span class="sxs-lookup"><span data-stu-id="eee74-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="eee74-129">幅の式を評価\*.075、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="eee74-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

