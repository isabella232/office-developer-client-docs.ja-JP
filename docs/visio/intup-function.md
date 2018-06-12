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
description: 次の整数に切り上げます。
ms.openlocfilehash: f54a08fa059d50102a6377b7e368e7e388297acc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805609"
---
# <a name="intup-function"></a><span data-ttu-id="38da6-103">INTUP 関数</span><span class="sxs-lookup"><span data-stu-id="38da6-103">INTUP Function</span></span>

<span data-ttu-id="38da6-104">次の整数に切り上げます。</span><span class="sxs-lookup"><span data-stu-id="38da6-104">Rounds a number up to the next integer.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="38da6-105">構文</span><span class="sxs-lookup"><span data-stu-id="38da6-105">Syntax</span></span>

<span data-ttu-id="38da6-106">INTUP (* **番号** *)</span><span class="sxs-lookup"><span data-stu-id="38da6-106">INTUP(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="38da6-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="38da6-107">Parameters</span></span>

|<span data-ttu-id="38da6-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="38da6-108">**Name**</span></span>|<span data-ttu-id="38da6-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="38da6-109">**Required/Optional**</span></span>|<span data-ttu-id="38da6-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="38da6-110">**Data Type**</span></span>|<span data-ttu-id="38da6-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="38da6-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="38da6-112">_number_</span><span class="sxs-lookup"><span data-stu-id="38da6-112">_number_</span></span> <br/> |<span data-ttu-id="38da6-113">必須</span><span class="sxs-lookup"><span data-stu-id="38da6-113">Required</span></span>  <br/> |<span data-ttu-id="38da6-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="38da6-114">**Number**</span></span> <br/> |<span data-ttu-id="38da6-115">切り上げの対象となる数値を指定します。</span><span class="sxs-lookup"><span data-stu-id="38da6-115">The number to round up.</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="38da6-116">例 1</span><span class="sxs-lookup"><span data-stu-id="38da6-116">Example 1</span></span>

<span data-ttu-id="38da6-117">INTUP(3.2)</span><span class="sxs-lookup"><span data-stu-id="38da6-117">INTUP(3.2)</span></span>
  
<span data-ttu-id="38da6-118">4 を返します。</span><span class="sxs-lookup"><span data-stu-id="38da6-118">Returns 4.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="38da6-119">例 2</span><span class="sxs-lookup"><span data-stu-id="38da6-119">Example 2</span></span>

<span data-ttu-id="38da6-120">INTUP(-3.2)</span><span class="sxs-lookup"><span data-stu-id="38da6-120">INTUP(-3.2)</span></span>
  
<span data-ttu-id="38da6-121">-3 を返します。</span><span class="sxs-lookup"><span data-stu-id="38da6-121">Returns -3.</span></span>
  
## <a name="example-3"></a><span data-ttu-id="38da6-122">例 3</span><span class="sxs-lookup"><span data-stu-id="38da6-122">Example 3</span></span>

<span data-ttu-id="38da6-123">INTUP(3)</span><span class="sxs-lookup"><span data-stu-id="38da6-123">INTUP(3)</span></span>
  
<span data-ttu-id="38da6-124">3 を返します。</span><span class="sxs-lookup"><span data-stu-id="38da6-124">Returns 3.</span></span>
  

