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
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293507"
---
# <a name="asin-function"></a><span data-ttu-id="b5f71-103">ASIN 関数</span><span class="sxs-lookup"><span data-stu-id="b5f71-103">ASIN Function</span></span>

<span data-ttu-id="b5f71-104">数値のアークサイン (正弦が  *数値*  である角度など) を返します。</span><span class="sxs-lookup"><span data-stu-id="b5f71-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="b5f71-105">構文</span><span class="sxs-lookup"><span data-stu-id="b5f71-105">Syntax</span></span>

<span data-ttu-id="b5f71-106">アークサイン (***数値*** )</span><span class="sxs-lookup"><span data-stu-id="b5f71-106">ASIN(***number*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="b5f71-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="b5f71-107">Parameters</span></span>

|<span data-ttu-id="b5f71-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="b5f71-108">**Name**</span></span>|<span data-ttu-id="b5f71-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="b5f71-109">**Required/Optional**</span></span>|<span data-ttu-id="b5f71-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="b5f71-110">**Data Type**</span></span>|<span data-ttu-id="b5f71-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="b5f71-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="b5f71-112">_number_</span><span class="sxs-lookup"><span data-stu-id="b5f71-112">_number_</span></span> <br/> |<span data-ttu-id="b5f71-113">必須</span><span class="sxs-lookup"><span data-stu-id="b5f71-113">Required</span></span>  <br/> |<span data-ttu-id="b5f71-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="b5f71-114">**Numeric**</span></span> <br/> |<span data-ttu-id="b5f71-115">角度のサインを指定します。</span><span class="sxs-lookup"><span data-stu-id="b5f71-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b5f71-116">解説</span><span class="sxs-lookup"><span data-stu-id="b5f71-116">Remarks</span></span>

<span data-ttu-id="b5f71-117">入力値は、-1 <=  *数値*  <= 1、または #NUM である必要があります。</span><span class="sxs-lookup"><span data-stu-id="b5f71-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="b5f71-118">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="b5f71-118">error is returned.</span></span> <span data-ttu-id="b5f71-119">その結果、角度は-π/2 <=  *angle*  <= π/2 ラジアン (-90 <=  *角度*  <= 90 度) になります。</span><span class="sxs-lookup"><span data-stu-id="b5f71-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="b5f71-120">例</span><span class="sxs-lookup"><span data-stu-id="b5f71-120">Example</span></span>

<span data-ttu-id="b5f71-121">アークサイン (1)</span><span class="sxs-lookup"><span data-stu-id="b5f71-121">ASIN(1)</span></span>
  
<span data-ttu-id="b5f71-122">90°を返します</span><span class="sxs-lookup"><span data-stu-id="b5f71-122">Returns 90 deg</span></span>
  

