---
title: TINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: int パラメーターで指定された正または負の値で明度を増やして色を変更します。
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280932"
---
# <a name="tint-function"></a><span data-ttu-id="a8966-103">TINT 関数</span><span class="sxs-lookup"><span data-stu-id="a8966-103">TINT Function</span></span>

<span data-ttu-id="a8966-104">_int_パラメーターで指定された正または負の値で明度を増やして色を変更します。</span><span class="sxs-lookup"><span data-stu-id="a8966-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a8966-105">構文</span><span class="sxs-lookup"><span data-stu-id="a8966-105">Syntax</span></span>

<span data-ttu-id="a8966-106">濃淡 (\* \* *color* \* *、* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a8966-106">TINT(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a8966-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a8966-107">Parameters</span></span>

|<span data-ttu-id="a8966-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="a8966-108">**Name**</span></span>|<span data-ttu-id="a8966-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a8966-109">**Required/Optional**</span></span>|<span data-ttu-id="a8966-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a8966-110">**Data Type**</span></span>|<span data-ttu-id="a8966-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="a8966-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a8966-112">_color_</span><span class="sxs-lookup"><span data-stu-id="a8966-112">_color_</span></span> <br/> |<span data-ttu-id="a8966-113">必須</span><span class="sxs-lookup"><span data-stu-id="a8966-113">Required</span></span>  <br/> |<span data-ttu-id="a8966-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="a8966-114">**Numeric**</span></span> <br/> |<span data-ttu-id="a8966-115">Microsoft Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="a8966-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="a8966-116">_int_</span><span class="sxs-lookup"><span data-stu-id="a8966-116">_int_</span></span> <br/> |<span data-ttu-id="a8966-117">必須</span><span class="sxs-lookup"><span data-stu-id="a8966-117">Required</span></span>  <br/> |<span data-ttu-id="a8966-118">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="a8966-118">**Integer**</span></span> <br/> |<span data-ttu-id="a8966-119">色の輝度を増加する量を指定します。</span><span class="sxs-lookup"><span data-stu-id="a8966-119">The amount by which to increase the luminosity of the color.</span></span> <span data-ttu-id="a8966-120">正または負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="a8966-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a8966-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="a8966-121">Return value</span></span>

 <span data-ttu-id="a8966-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="a8966-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8966-123">解説</span><span class="sxs-lookup"><span data-stu-id="a8966-123">Remarks</span></span>

<span data-ttu-id="a8966-124">明度の上限と下限は、それぞれ 0 と 240 です。</span><span class="sxs-lookup"><span data-stu-id="a8966-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="a8966-125">_int_パラメーターに渡すことができる整数のサイズに制限はありませんが、明度がこれらの制限を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="a8966-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

