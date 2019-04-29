---
title: INTUP 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251446
localization_priority: Normal
ms.assetid: ce193ce1-c7fd-6609-ad37-a3a28b30a1bd
description: 数値を次の整数に切り上げます。
ms.openlocfilehash: 405345ae1d22d599df85e2a640445c8c681ec2f6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416140"
---
# <a name="intup-function"></a><span data-ttu-id="e7ab4-103">INTUP 関数</span><span class="sxs-lookup"><span data-stu-id="e7ab4-103">INTUP Function</span></span>

<span data-ttu-id="e7ab4-104">数値を次の整数に切り上げます。</span><span class="sxs-lookup"><span data-stu-id="e7ab4-104">Rounds a number up to the next integer.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="e7ab4-105">構文</span><span class="sxs-lookup"><span data-stu-id="e7ab4-105">Syntax</span></span>

<span data-ttu-id="e7ab4-106">intup (\* \* *number* \* \*)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-106">INTUP(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e7ab4-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="e7ab4-107">Parameters</span></span>

|<span data-ttu-id="e7ab4-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-108">**Name**</span></span>|<span data-ttu-id="e7ab4-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-109">**Required/Optional**</span></span>|<span data-ttu-id="e7ab4-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-110">**Data Type**</span></span>|<span data-ttu-id="e7ab4-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e7ab4-112">_number_</span><span class="sxs-lookup"><span data-stu-id="e7ab4-112">_number_</span></span> <br/> |<span data-ttu-id="e7ab4-113">必須</span><span class="sxs-lookup"><span data-stu-id="e7ab4-113">Required</span></span>  <br/> |<span data-ttu-id="e7ab4-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="e7ab4-114">**Number**</span></span> <br/> |<span data-ttu-id="e7ab4-115">切り上げの対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="e7ab4-115">The number to round up.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="e7ab4-116">例 1</span><span class="sxs-lookup"><span data-stu-id="e7ab4-116">Example 1</span></span>

<span data-ttu-id="e7ab4-117">intup (3.2)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-117">INTUP(3.2)</span></span>
  
<span data-ttu-id="e7ab4-118">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="e7ab4-118">Returns 4.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="e7ab4-119">例 2</span><span class="sxs-lookup"><span data-stu-id="e7ab4-119">Example 2</span></span>

<span data-ttu-id="e7ab4-120">intup (-3.2)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-120">INTUP(-3.2)</span></span>
  
<span data-ttu-id="e7ab4-121">-3 を返します。</span><span class="sxs-lookup"><span data-stu-id="e7ab4-121">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="e7ab4-122">例 3</span><span class="sxs-lookup"><span data-stu-id="e7ab4-122">Example 3</span></span>

<span data-ttu-id="e7ab4-123">intup (3)</span><span class="sxs-lookup"><span data-stu-id="e7ab4-123">INTUP(3)</span></span>
  
<span data-ttu-id="e7ab4-124">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="e7ab4-124">Returns 3.</span></span>
  

