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
description: そのサインが number である角度など、数値のアークサインを返します。
ms.openlocfilehash: e5ed8f9fc8c85ac4816fede03bfe6f6af5cbf5f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804808"
---
# <a name="asin-function"></a><span data-ttu-id="9958a-103">ASIN 関数</span><span class="sxs-lookup"><span data-stu-id="9958a-103">ASIN Function</span></span>

<span data-ttu-id="9958a-104">そのサインが*数値*である角度など、数値のアークサインを返します。</span><span class="sxs-lookup"><span data-stu-id="9958a-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="9958a-105">構文</span><span class="sxs-lookup"><span data-stu-id="9958a-105">Syntax</span></span>

<span data-ttu-id="9958a-106">ASIN (* **番号** *)</span><span class="sxs-lookup"><span data-stu-id="9958a-106">ASIN(** *number* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="9958a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="9958a-107">Parameters</span></span>

|<span data-ttu-id="9958a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="9958a-108">**Name**</span></span>|<span data-ttu-id="9958a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="9958a-109">**Required/Optional**</span></span>|<span data-ttu-id="9958a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="9958a-110">**Data Type**</span></span>|<span data-ttu-id="9958a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="9958a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="9958a-112">_number_</span><span class="sxs-lookup"><span data-stu-id="9958a-112">_number_</span></span> <br/> |<span data-ttu-id="9958a-113">必須</span><span class="sxs-lookup"><span data-stu-id="9958a-113">Required</span></span>  <br/> |<span data-ttu-id="9958a-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="9958a-114">**Numeric**</span></span> <br/> |<span data-ttu-id="9958a-115">角度のサインを指定します。</span><span class="sxs-lookup"><span data-stu-id="9958a-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9958a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="9958a-116">Remarks</span></span>

<span data-ttu-id="9958a-117">入力値が-1 の範囲である必要があります < =*数*< = 1、または、#NUM!</span><span class="sxs-lookup"><span data-stu-id="9958a-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="9958a-118">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="9958a-118">error is returned.</span></span> <span data-ttu-id="9958a-119">結果として得られる角度は -π/2 の範囲で、< =*角度*< = π/2 ラジアン (-90 < =*角度*< = 90 °)。</span><span class="sxs-lookup"><span data-stu-id="9958a-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="9958a-120">例</span><span class="sxs-lookup"><span data-stu-id="9958a-120">Example</span></span>

<span data-ttu-id="9958a-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="9958a-121">ASIN(1)</span></span>
  
<span data-ttu-id="9958a-122">90°を返します</span><span class="sxs-lookup"><span data-stu-id="9958a-122">Returns 90 deg</span></span>
  

