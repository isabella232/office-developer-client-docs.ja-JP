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
description: 数値のアークサイン (たとえば、サインが数値の角度) を返します。
ms.openlocfilehash: e66ed9ab3d01ac79bceb18f5c793afc928e5e4b4
ms.sourcegitcommit: 939bd9686ba41a8f94b82e004ed84b9054d9c7cf
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/28/2020
ms.locfileid: "48293507"
---
# <a name="asin-function"></a><span data-ttu-id="2998a-103">ASIN 関数</span><span class="sxs-lookup"><span data-stu-id="2998a-103">ASIN Function</span></span>

<span data-ttu-id="2998a-104">数値のアークサイン (たとえば、サインが数値の角度) を返  *します*  。</span><span class="sxs-lookup"><span data-stu-id="2998a-104">Returns the arcsine of a number, for example, the angle whose sine is  *number*  .</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="2998a-105">構文</span><span class="sxs-lookup"><span data-stu-id="2998a-105">Syntax</span></span>

<span data-ttu-id="2998a-106">ASIN(***number*** )</span><span class="sxs-lookup"><span data-stu-id="2998a-106">ASIN(***number*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2998a-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="2998a-107">Parameters</span></span>

|<span data-ttu-id="2998a-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="2998a-108">**Name**</span></span>|<span data-ttu-id="2998a-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="2998a-109">**Required/Optional**</span></span>|<span data-ttu-id="2998a-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="2998a-110">**Data Type**</span></span>|<span data-ttu-id="2998a-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="2998a-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2998a-112">_number_</span><span class="sxs-lookup"><span data-stu-id="2998a-112">_number_</span></span> <br/> |<span data-ttu-id="2998a-113">必須</span><span class="sxs-lookup"><span data-stu-id="2998a-113">Required</span></span>  <br/> |<span data-ttu-id="2998a-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="2998a-114">**Numeric**</span></span> <br/> |<span data-ttu-id="2998a-115">角度のサインを指定します。</span><span class="sxs-lookup"><span data-stu-id="2998a-115">The sine of the angle.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2998a-116">注釈</span><span class="sxs-lookup"><span data-stu-id="2998a-116">Remarks</span></span>

<span data-ttu-id="2998a-117">入力値は、-1 の範囲で指定する必要< *=*  <= 1、または #NUM!</span><span class="sxs-lookup"><span data-stu-id="2998a-117">The input value must be in the range -1 <=  *number*  <= 1, or a #NUM!</span></span> <span data-ttu-id="2998a-118">エラーを返します。</span><span class="sxs-lookup"><span data-stu-id="2998a-118">error is returned.</span></span> <span data-ttu-id="2998a-119">結果の角度は、-PI/2 <=  *角度*  <= PI/2 ラジアン (-90 < *=*  角度 <= 90 度) です。</span><span class="sxs-lookup"><span data-stu-id="2998a-119">The resulting angle is in the range -PI/2 <=  *angle*  <= PI/2 radians (-90 <=  *angle*  <= 90 degrees).</span></span> 
  
## <a name="example"></a><span data-ttu-id="2998a-120">例</span><span class="sxs-lookup"><span data-stu-id="2998a-120">Example</span></span>

<span data-ttu-id="2998a-121">ASIN(1)</span><span class="sxs-lookup"><span data-stu-id="2998a-121">ASIN(1)</span></span>
  
<span data-ttu-id="2998a-122">90°を返します</span><span class="sxs-lookup"><span data-stu-id="2998a-122">Returns 90 deg</span></span>
  

