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
description: 角度の範囲に正規化します。
ms.openlocfilehash: 01092e06b55c73953417fe7d0fa1c9f74d668922
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804767"
---
# <a name="ang360-function"></a><span data-ttu-id="21c89-103">ANG360 関数</span><span class="sxs-lookup"><span data-stu-id="21c89-103">ANG360 Function</span></span>

<span data-ttu-id="21c89-104">正規化の角度の範囲が 0 \<= 結果\<2PI ラジアン (0 \<= 結果\<360 °)。</span><span class="sxs-lookup"><span data-stu-id="21c89-104">Normalizes an angle's range to be 0 \<= result \< 2PI radians (0 \<= result \< 360 degrees).</span></span>
  
## <a name="syntax"></a><span data-ttu-id="21c89-105">構文</span><span class="sxs-lookup"><span data-stu-id="21c89-105">Syntax</span></span>

<span data-ttu-id="21c89-106">ANG360 (* **角度** *)</span><span class="sxs-lookup"><span data-stu-id="21c89-106">ANG360(** *angle* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="21c89-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="21c89-107">Parameters</span></span>

|<span data-ttu-id="21c89-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="21c89-108">**Name**</span></span>|<span data-ttu-id="21c89-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="21c89-109">**Required/Optional**</span></span>|<span data-ttu-id="21c89-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="21c89-110">**Data Type**</span></span>|<span data-ttu-id="21c89-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="21c89-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="21c89-112">_角度_</span><span class="sxs-lookup"><span data-stu-id="21c89-112">_angle_</span></span> <br/> |<span data-ttu-id="21c89-113">必須</span><span class="sxs-lookup"><span data-stu-id="21c89-113">Required</span></span>  <br/> |<span data-ttu-id="21c89-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="21c89-114">**Numeric**</span></span> <br/> |<span data-ttu-id="21c89-115">正規化する角度を指定します。</span><span class="sxs-lookup"><span data-stu-id="21c89-115">The angle to be normalized.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="21c89-116">注釈</span><span class="sxs-lookup"><span data-stu-id="21c89-116">Remarks</span></span>

<span data-ttu-id="21c89-117">角度の単位を使用して*角度*を指定しない場合はラジアンとして解釈されます。</span><span class="sxs-lookup"><span data-stu-id="21c89-117">If  *angle*  is not specified by using angular units, it is interpreted as radians.</span></span> <span data-ttu-id="21c89-118">*角度*は、#value! の値に変換できません。 場合、</span><span class="sxs-lookup"><span data-stu-id="21c89-118">If  *angle*  cannot be converted to a value, a #VALUE!</span></span> <span data-ttu-id="21c89-119">エラーが返されます。</span><span class="sxs-lookup"><span data-stu-id="21c89-119">error is returned.</span></span> 
  
## <a name="example-1"></a><span data-ttu-id="21c89-120">例 1</span><span class="sxs-lookup"><span data-stu-id="21c89-120">Example 1</span></span>

<span data-ttu-id="21c89-121">ANG360(395 deg)</span><span class="sxs-lookup"><span data-stu-id="21c89-121">ANG360(395 deg)</span></span>
  
<span data-ttu-id="21c89-122">35°を返します</span><span class="sxs-lookup"><span data-stu-id="21c89-122">Returns 35 deg</span></span>
  
## <a name="example-2"></a><span data-ttu-id="21c89-123">例 2</span><span class="sxs-lookup"><span data-stu-id="21c89-123">Example 2</span></span>

<span data-ttu-id="21c89-124">ANG360(-9.8 rad)</span><span class="sxs-lookup"><span data-stu-id="21c89-124">ANG360(-9.8 rad)</span></span>
  
<span data-ttu-id="21c89-125">2.7664 ラジアンを返します</span><span class="sxs-lookup"><span data-stu-id="21c89-125">Returns 2.7664 rad</span></span>
  
## <a name="example-3"></a><span data-ttu-id="21c89-126">例 3</span><span class="sxs-lookup"><span data-stu-id="21c89-126">Example 3</span></span>

<span data-ttu-id="21c89-127">ANG360(45)</span><span class="sxs-lookup"><span data-stu-id="21c89-127">ANG360(45)</span></span>
  
<span data-ttu-id="21c89-128">58.31° (1.0177 ラジアン) を返します</span><span class="sxs-lookup"><span data-stu-id="21c89-128">Returns 58.31 deg (1.0177 rad)</span></span>
  

