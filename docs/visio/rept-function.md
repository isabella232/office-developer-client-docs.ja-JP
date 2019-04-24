---
title: REPT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027335
localization_priority: Normal
ms.assetid: 53362a32-ac27-42a3-ace1-c6184ab20b52
description: 文字列を指定された回数だけ繰り返して表示します。
ms.openlocfilehash: 84e7167fcee426c607e6967aff0530362685dd35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326804"
---
# <a name="rept-function"></a><span data-ttu-id="1fc3d-103">REPT 関数</span><span class="sxs-lookup"><span data-stu-id="1fc3d-103">REPT Function</span></span>

<span data-ttu-id="1fc3d-104">文字列を指定された回数だけ繰り返して表示します。</span><span class="sxs-lookup"><span data-stu-id="1fc3d-104">Repeats text a given number of times.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="1fc3d-105">構文</span><span class="sxs-lookup"><span data-stu-id="1fc3d-105">Syntax</span></span>

<span data-ttu-id="1fc3d-106">REPT (\* \* *text* \* *、* **繰り返し回数** \*)</span><span class="sxs-lookup"><span data-stu-id="1fc3d-106">REPT (\*\* *text* \*\*, \*\* *number_times* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="1fc3d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="1fc3d-107">Parameters</span></span>

|<span data-ttu-id="1fc3d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="1fc3d-108">**Name**</span></span>|<span data-ttu-id="1fc3d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="1fc3d-109">**Required/Optional**</span></span>|<span data-ttu-id="1fc3d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="1fc3d-110">**Data Type**</span></span>|<span data-ttu-id="1fc3d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="1fc3d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="1fc3d-112">_text_</span><span class="sxs-lookup"><span data-stu-id="1fc3d-112">_text_</span></span> <br/> |<span data-ttu-id="1fc3d-113">必須</span><span class="sxs-lookup"><span data-stu-id="1fc3d-113">Required</span></span>  <br/> |<span data-ttu-id="1fc3d-114">**String**</span><span class="sxs-lookup"><span data-stu-id="1fc3d-114">**String**</span></span> <br/> | <span data-ttu-id="1fc3d-115">繰り返す文字列を指定します。</span><span class="sxs-lookup"><span data-stu-id="1fc3d-115">The text you want to repeat.</span></span>  <br/> |
| <span data-ttu-id="1fc3d-116">_繰り返し回数_</span><span class="sxs-lookup"><span data-stu-id="1fc3d-116">_number_times_</span></span> <br/> |<span data-ttu-id="1fc3d-117">必須</span><span class="sxs-lookup"><span data-stu-id="1fc3d-117">Required</span></span>  <br/> |<span data-ttu-id="1fc3d-118">**数値**</span><span class="sxs-lookup"><span data-stu-id="1fc3d-118">**Number**</span></span> <br/> |<span data-ttu-id="1fc3d-119">文字列の繰り返す回数を、正の数値で指定します。</span><span class="sxs-lookup"><span data-stu-id="1fc3d-119">A positive number specifying the number of times to repeat text.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fc3d-120">解説</span><span class="sxs-lookup"><span data-stu-id="1fc3d-120">Remarks</span></span>

<span data-ttu-id="1fc3d-121">*繰り返し回数*:</span><span class="sxs-lookup"><span data-stu-id="1fc3d-121">If  *number_times*  is:</span></span> 
  
- <span data-ttu-id="1fc3d-122">number_times がゼロ (0) の場合、"" (空文字列) を返します。</span><span class="sxs-lookup"><span data-stu-id="1fc3d-122">Zero (0), REPT returns "" (empty text).</span></span>
    
- <span data-ttu-id="1fc3d-123">number_times が整数でない場合、小数点以下は切り捨てられます。</span><span class="sxs-lookup"><span data-stu-id="1fc3d-123">Not an interger, it is truncated.</span></span>
    
## <a name="example"></a><span data-ttu-id="1fc3d-124">例</span><span class="sxs-lookup"><span data-stu-id="1fc3d-124">Example</span></span>

<span data-ttu-id="1fc3d-125">REPT ("\*", 5)</span><span class="sxs-lookup"><span data-stu-id="1fc3d-125">REPT ("\*", 5)</span></span> 
  
<span data-ttu-id="1fc3d-126">を\* \* \*返し\*ます\*。</span><span class="sxs-lookup"><span data-stu-id="1fc3d-126">Returns \*\*\*\*\*.</span></span> 
  

