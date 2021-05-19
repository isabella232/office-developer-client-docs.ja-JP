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
description: 状態の値に応じて、2 つの式の 1 つを評価します。
ms.openlocfilehash: 544bb2b19dc610591afc78c407301098fac9c7c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420347"
---
# <a name="userui-function"></a><span data-ttu-id="2dedb-103">USERUI 関数</span><span class="sxs-lookup"><span data-stu-id="2dedb-103">USERUI Function</span></span>

<span data-ttu-id="2dedb-104">状態の値に応じて、2 つの式の 1 つを評価  _します_。</span><span class="sxs-lookup"><span data-stu-id="2dedb-104">Evaluates one of the two expressions depending on the value of  _state_.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2dedb-105">構文</span><span class="sxs-lookup"><span data-stu-id="2dedb-105">Syntax</span></span>

<span data-ttu-id="2dedb-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span><span class="sxs-lookup"><span data-stu-id="2dedb-106">USERUI(\*\* *state* \*\*, \*\* *defaultexpression* \*\*, \*\* *userexpression* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2dedb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2dedb-107">Parameters</span></span>

|<span data-ttu-id="2dedb-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="2dedb-108">**Name**</span></span>|<span data-ttu-id="2dedb-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="2dedb-109">**Required/Optional**</span></span>|<span data-ttu-id="2dedb-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="2dedb-110">**Data Type**</span></span>|<span data-ttu-id="2dedb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2dedb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2dedb-112">_state_</span><span class="sxs-lookup"><span data-stu-id="2dedb-112">_state_</span></span> <br/> |<span data-ttu-id="2dedb-113">必須</span><span class="sxs-lookup"><span data-stu-id="2dedb-113">Required</span></span>  <br/> |<span data-ttu-id="2dedb-114">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="2dedb-114">**Boolean**</span></span> <br/> |<span data-ttu-id="2dedb-115">評価する式を決定します。</span><span class="sxs-lookup"><span data-stu-id="2dedb-115">Determines which expression to evaluate.</span></span>  <br/> |
| <span data-ttu-id="2dedb-116">_defaultexpression_</span><span class="sxs-lookup"><span data-stu-id="2dedb-116">_defaultexpression_</span></span> <br/> |<span data-ttu-id="2dedb-117">必須</span><span class="sxs-lookup"><span data-stu-id="2dedb-117">Required</span></span>  <br/> |<span data-ttu-id="2dedb-118">**String**</span><span class="sxs-lookup"><span data-stu-id="2dedb-118">**String**</span></span> <br/> |<span data-ttu-id="2dedb-119">既定の式。</span><span class="sxs-lookup"><span data-stu-id="2dedb-119">The default expression.</span></span>  <br/> |
| <span data-ttu-id="2dedb-120">_userexpression_</span><span class="sxs-lookup"><span data-stu-id="2dedb-120">_userexpression_</span></span> <br/> |<span data-ttu-id="2dedb-121">必須</span><span class="sxs-lookup"><span data-stu-id="2dedb-121">Required</span></span>  <br/> |<span data-ttu-id="2dedb-122">**String**</span><span class="sxs-lookup"><span data-stu-id="2dedb-122">**String**</span></span> <br/> |<span data-ttu-id="2dedb-123">ユーザーが指定した式。</span><span class="sxs-lookup"><span data-stu-id="2dedb-123">An expression supplied by the user.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2dedb-124">注釈</span><span class="sxs-lookup"><span data-stu-id="2dedb-124">Remarks</span></span>

<span data-ttu-id="2dedb-125">state  _が_ 0 の場合、USERUI 関数は  _defaultexpression を評価します_。</span><span class="sxs-lookup"><span data-stu-id="2dedb-125">If  _state_ is 0, the USERUI function evaluates the  _defaultexpression_.</span></span> <span data-ttu-id="2dedb-126">状態  _が_ 1 の場合  _、userexpression が評価されます_。</span><span class="sxs-lookup"><span data-stu-id="2dedb-126">If  _state_ is 1, it evaluates the  _userexpression_.</span></span>
  
## <a name="example"></a><span data-ttu-id="2dedb-127">例</span><span class="sxs-lookup"><span data-stu-id="2dedb-127">Example</span></span>

<span data-ttu-id="2dedb-128">USERUI(1, if(Width \> 6in, 6in, Width), Width \* 0.75)</span><span class="sxs-lookup"><span data-stu-id="2dedb-128">USERUI(1, if(Width\>6in, 6in, Width), Width\*0.75)</span></span> 
  
<span data-ttu-id="2dedb-129">Width \* .075 という式を評価し、結果を返します。</span><span class="sxs-lookup"><span data-stu-id="2dedb-129">Evaluates the expression Width\*.075 and returns the result.</span></span> 
  

