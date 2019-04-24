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
ms.openlocfilehash: 017dd89bd3b814c10422cd32eea1ee7e343eaf50
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341490"
---
# <a name="ang360-function"></a><span data-ttu-id="747b8-103">ANG360 関数</span><span class="sxs-lookup"><span data-stu-id="747b8-103">ANG360 Function</span></span>

<span data-ttu-id="747b8-104">角度の\<範囲を 0 = result \< 2pi ラジアンに正規化します\<(0 \< = result 360 度)。</span><span class="sxs-lookup"><span data-stu-id="747b8-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="747b8-105">構文</span><span class="sxs-lookup"><span data-stu-id="747b8-105">Syntax</span></span>

<span data-ttu-id="747b8-106">ANG360 (\* \* *angle* \* \*)</span><span class="sxs-lookup"><span data-stu-id="747b8-106">ANG360(\*\* *angle* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="747b8-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="747b8-107">Parameters</span></span>

|<span data-ttu-id="747b8-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="747b8-108">**Name**</span></span>|<span data-ttu-id="747b8-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="747b8-109">**Required/Optional**</span></span>|<span data-ttu-id="747b8-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="747b8-110">**Data Type**</span></span>|<span data-ttu-id="747b8-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="747b8-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="747b8-112">_直交_</span><span class="sxs-lookup"><span data-stu-id="747b8-112">_angle_</span></span> <br/> |<span data-ttu-id="747b8-113">必須</span><span class="sxs-lookup"><span data-stu-id="747b8-113">Required</span></span>  <br/> |<span data-ttu-id="747b8-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="747b8-114">**Numeric**</span></span> <br/> |<span data-ttu-id="747b8-115">正規化する角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="747b8-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="747b8-116">解説</span><span class="sxs-lookup"><span data-stu-id="747b8-116">Remarks</span></span>

<span data-ttu-id="747b8-117">角度を指定しない場合、*角度*はラジアンとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="747b8-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="747b8-118">*角度*を値に変換できない場合は、#VALUE します。</span><span class="sxs-lookup"><span data-stu-id="747b8-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="747b8-119">を返します。</span><span class="sxs-lookup"><span data-stu-id="747b8-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="747b8-120">例 1</span><span class="sxs-lookup"><span data-stu-id="747b8-120">Example 1</span></span>

<span data-ttu-id="747b8-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="747b8-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="747b8-122">35°を返します</span><span class="sxs-lookup"><span data-stu-id="747b8-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="747b8-123">例 2</span><span class="sxs-lookup"><span data-stu-id="747b8-123">Example 2</span></span>

<span data-ttu-id="747b8-124">ANG360(-9.8 rad)</span><span class="sxs-lookup"><span data-stu-id="747b8-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="747b8-125">2.7664 ラジアンを返します</span><span class="sxs-lookup"><span data-stu-id="747b8-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="747b8-126">例 3</span><span class="sxs-lookup"><span data-stu-id="747b8-126">Example 3</span></span>

<span data-ttu-id="747b8-127">ANG360 (45)</span><span class="sxs-lookup"><span data-stu-id="747b8-127">ANG360(45)</span></span>
  
<span data-ttu-id="747b8-128">58.31° (1.0177 ラジアン) を返します</span><span class="sxs-lookup"><span data-stu-id="747b8-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

