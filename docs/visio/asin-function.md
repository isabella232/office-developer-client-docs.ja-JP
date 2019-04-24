---
title: ASIN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251395
localization_priority: Normal
ms.assetid: 7d917be4-65b1-002f-48cc-6d81916a1157
description: 数値のアークサイン (正弦が数値である角度など) を返します。
ms.openlocfilehash: a7585dc07053466203f11cc04ce249ceb62fbda0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341525"
---
# <a name="asin-function"></a><span data-ttu-id="bc5d1-103">ASIN 関数</span><span class="sxs-lookup"><span data-stu-id="bc5d1-103">ASIN Function</span></span>

<span data-ttu-id="bc5d1-104">数値のアークサイン (正弦が*数値*である角度など) を返します。</span><span class="sxs-lookup"><span data-stu-id="bc5d1-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="bc5d1-105">構文</span><span class="sxs-lookup"><span data-stu-id="bc5d1-105">Syntax</span></span>

<span data-ttu-id="bc5d1-106">アークサイン (\* **数値** \*)</span><span class="sxs-lookup"><span data-stu-id="bc5d1-106">ASIN(\*\* *number* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="bc5d1-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="bc5d1-107">Parameters</span></span>

|<span data-ttu-id="bc5d1-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="bc5d1-108">**Name**</span></span>|<span data-ttu-id="bc5d1-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="bc5d1-109">**Required/Optional**</span></span>|<span data-ttu-id="bc5d1-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="bc5d1-110">**Data Type**</span></span>|<span data-ttu-id="bc5d1-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="bc5d1-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="bc5d1-112">_number_</span><span class="sxs-lookup"><span data-stu-id="bc5d1-112">_number_</span></span> <br/> |<span data-ttu-id="bc5d1-113">必須</span><span class="sxs-lookup"><span data-stu-id="bc5d1-113">Required</span></span>  <br/> |<span data-ttu-id="bc5d1-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="bc5d1-114">**Numeric**</span></span> <br/> |<span data-ttu-id="bc5d1-115">角度のサインを指定します。</span><span class="sxs-lookup"><span data-stu-id="bc5d1-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bc5d1-116">解説</span><span class="sxs-lookup"><span data-stu-id="bc5d1-116">Remarks</span></span>

<span data-ttu-id="bc5d1-117">入力値は、-1 < = *number* < = 1、または #NUM の範囲内である必要があります。</span><span class="sxs-lookup"><span data-stu-id="bc5d1-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="bc5d1-118">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="bc5d1-118">error is returned.</span></span> <span data-ttu-id="bc5d1-119">結果の角度は、-pi/2 < = *angle* < = π/2 ラジアン (-90 < = *angle* < = 90 °) の範囲になります。</span><span class="sxs-lookup"><span data-stu-id="bc5d1-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="bc5d1-120">例</span><span class="sxs-lookup"><span data-stu-id="bc5d1-120">Example</span></span>

<span data-ttu-id="bc5d1-121">アークサイン (1)</span><span class="sxs-lookup"><span data-stu-id="bc5d1-121">ASIN(1)</span></span>
  
<span data-ttu-id="bc5d1-122">90°を返します</span><span class="sxs-lookup"><span data-stu-id="bc5d1-122">Returns 90 deg</span></span>
  

