---
title: SUM 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251501
localization_priority: Normal
ms.assetid: fc97cef7-59c3-5be1-34fe-a40b4b33d1d6
description: 数値のリストの合計を返します。
ms.openlocfilehash: a64de440868c055ed917b7646a7c1d81318e3eff
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806591"
---
# <a name="sum-function"></a><span data-ttu-id="66ba5-103">SUM 関数</span><span class="sxs-lookup"><span data-stu-id="66ba5-103">SUM Function</span></span>

<span data-ttu-id="66ba5-104">数値のリストの合計を返します。</span><span class="sxs-lookup"><span data-stu-id="66ba5-104">Returns the sum of a list of numbers.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="66ba5-105">構文</span><span class="sxs-lookup"><span data-stu-id="66ba5-105">Syntax</span></span>

<span data-ttu-id="66ba5-106">合計 (* * *[数値 1]* * *、* **数値 2* * *,...、* * *[numberN]* * *)</span><span class="sxs-lookup"><span data-stu-id="66ba5-106">SUM(** *number1* **, ** *number2* **,..., ** *[numberN]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="66ba5-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="66ba5-107">Parameters</span></span>

|<span data-ttu-id="66ba5-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="66ba5-108">**Name**</span></span>|<span data-ttu-id="66ba5-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="66ba5-109">**Required/Optional**</span></span>|<span data-ttu-id="66ba5-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="66ba5-110">**Data Type**</span></span>|<span data-ttu-id="66ba5-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="66ba5-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="66ba5-112">_number1_</span><span class="sxs-lookup"><span data-stu-id="66ba5-112">_number1_</span></span> <br/> |<span data-ttu-id="66ba5-113">必須</span><span class="sxs-lookup"><span data-stu-id="66ba5-113">Required</span></span>  <br/> |<span data-ttu-id="66ba5-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="66ba5-114">**Numeric**</span></span> <br/> |<span data-ttu-id="66ba5-115">最初の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66ba5-115">The first number.</span></span>  <br/> |
| <span data-ttu-id="66ba5-116">_number2_</span><span class="sxs-lookup"><span data-stu-id="66ba5-116">_number2_</span></span> <br/> |<span data-ttu-id="66ba5-117">必須</span><span class="sxs-lookup"><span data-stu-id="66ba5-117">Required</span></span>  <br/> |<span data-ttu-id="66ba5-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="66ba5-118">**Numeric**</span></span> <br/> |<span data-ttu-id="66ba5-119">2 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66ba5-119">The second number.</span></span>  <br/> |
| <span data-ttu-id="66ba5-120">_numberN_</span><span class="sxs-lookup"><span data-stu-id="66ba5-120">_numberN_</span></span> <br/> |<span data-ttu-id="66ba5-121">省略可能</span><span class="sxs-lookup"><span data-stu-id="66ba5-121">Optional</span></span>  <br/> |<span data-ttu-id="66ba5-122">**数値**</span><span class="sxs-lookup"><span data-stu-id="66ba5-122">**Numeric**</span></span> <br/> |<span data-ttu-id="66ba5-123">n 番目の数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="66ba5-123">The nth number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="66ba5-124">�߂�l</span><span class="sxs-lookup"><span data-stu-id="66ba5-124">Return value</span></span>

<span data-ttu-id="66ba5-125">数値型 (Numeric)</span><span class="sxs-lookup"><span data-stu-id="66ba5-125">Numeric</span></span>
  
## <a name="example"></a><span data-ttu-id="66ba5-126">例</span><span class="sxs-lookup"><span data-stu-id="66ba5-126">Example</span></span>

<span data-ttu-id="66ba5-127">SUM(5,7,12)</span><span class="sxs-lookup"><span data-stu-id="66ba5-127">SUM(5,7,12)</span></span>
  
<span data-ttu-id="66ba5-128">24 を返します。</span><span class="sxs-lookup"><span data-stu-id="66ba5-128">Returns 24.</span></span>
  

