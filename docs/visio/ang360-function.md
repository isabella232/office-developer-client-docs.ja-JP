---
title: ANG360 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251392
localization_priority: Normal
ms.assetid: 23e6899d-0a94-a7d8-8de2-091e0531f163
description: 角度の範囲を正規化します。
ms.openlocfilehash: 6916e50daad735843bf0a2a6361fb5b1b833e2ce
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160301"
---
# <a name="ang360-function"></a><span data-ttu-id="12d60-103">ANG360 関数</span><span class="sxs-lookup"><span data-stu-id="12d60-103">ANG360 Function</span></span>

<span data-ttu-id="12d60-104">角度の範囲を 0 = 結果 \< \< 2PI ラジアン (0 = 結果 \< \< 360 度) に正規化します。</span><span class="sxs-lookup"><span data-stu-id="12d60-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="12d60-105">構文</span><span class="sxs-lookup"><span data-stu-id="12d60-105">Syntax</span></span>

<span data-ttu-id="12d60-106">ANG360(***angle*** )</span><span class="sxs-lookup"><span data-stu-id="12d60-106">ANG360(***angle*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="12d60-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="12d60-107">Parameters</span></span>

|<span data-ttu-id="12d60-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="12d60-108">**Name**</span></span>|<span data-ttu-id="12d60-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="12d60-109">**Required/Optional**</span></span>|<span data-ttu-id="12d60-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="12d60-110">**Data Type**</span></span>|<span data-ttu-id="12d60-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="12d60-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="12d60-112">_angle_</span><span class="sxs-lookup"><span data-stu-id="12d60-112">_angle_</span></span> <br/> |<span data-ttu-id="12d60-113">必須</span><span class="sxs-lookup"><span data-stu-id="12d60-113">Required</span></span>  <br/> |<span data-ttu-id="12d60-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="12d60-114">**Numeric**</span></span> <br/> |<span data-ttu-id="12d60-115">正規化する角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="12d60-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12d60-116">注釈</span><span class="sxs-lookup"><span data-stu-id="12d60-116">Remarks</span></span>

<span data-ttu-id="12d60-117">角度  *単位*  を使用して角度を指定しない場合は、ラジアンとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="12d60-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="12d60-118">angle  *を*  値に変換できない場合は、値#VALUE!</span><span class="sxs-lookup"><span data-stu-id="12d60-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="12d60-119">を返します。</span><span class="sxs-lookup"><span data-stu-id="12d60-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="12d60-120">例 1</span><span class="sxs-lookup"><span data-stu-id="12d60-120">Example 1</span></span>

<span data-ttu-id="12d60-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="12d60-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="12d60-122">35°を返します</span><span class="sxs-lookup"><span data-stu-id="12d60-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="12d60-123">例 2</span><span class="sxs-lookup"><span data-stu-id="12d60-123">Example 2</span></span>

<span data-ttu-id="12d60-124">ANG360(-9.8 rad)</span><span class="sxs-lookup"><span data-stu-id="12d60-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="12d60-125">2.7664 ラジアンを返します</span><span class="sxs-lookup"><span data-stu-id="12d60-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="12d60-126">例 3</span><span class="sxs-lookup"><span data-stu-id="12d60-126">Example 3</span></span>

<span data-ttu-id="12d60-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="12d60-127">ANG360(45)</span></span>
  
<span data-ttu-id="12d60-128">58.31° (1.0177 ラジアン) を返します</span><span class="sxs-lookup"><span data-stu-id="12d60-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

