---
title: TINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: Int パラメーターで指定した量 (正または負) で明度を上げて色を変更します。
ms.openlocfilehash: a4b15596a4742edb4f9e4746929f19d2eafe94d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806665"
---
# <a name="tint-function"></a><span data-ttu-id="28d4b-103">TINT 関数</span><span class="sxs-lookup"><span data-stu-id="28d4b-103">TINT Function</span></span>

<span data-ttu-id="28d4b-104">_Int_パラメーターで指定した量 (正または負) で明度を上げて色を変更します。</span><span class="sxs-lookup"><span data-stu-id="28d4b-104">Modifies the color by increasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="28d4b-105">構文</span><span class="sxs-lookup"><span data-stu-id="28d4b-105">Syntax</span></span>

<span data-ttu-id="28d4b-106">濃淡 (* **色** *、* * *int* * *)</span><span class="sxs-lookup"><span data-stu-id="28d4b-106">TINT(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="28d4b-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="28d4b-107">Parameters</span></span>

|<span data-ttu-id="28d4b-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="28d4b-108">**Name**</span></span>|<span data-ttu-id="28d4b-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="28d4b-109">**Required/Optional**</span></span>|<span data-ttu-id="28d4b-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="28d4b-110">**Data Type**</span></span>|<span data-ttu-id="28d4b-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="28d4b-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="28d4b-112">_color_</span><span class="sxs-lookup"><span data-stu-id="28d4b-112">_color_</span></span> <br/> |<span data-ttu-id="28d4b-113">必須</span><span class="sxs-lookup"><span data-stu-id="28d4b-113">Required</span></span>  <br/> |<span data-ttu-id="28d4b-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="28d4b-114">**Numeric**</span></span> <br/> |<span data-ttu-id="28d4b-115">Microsoft Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="28d4b-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="28d4b-116">_int_</span><span class="sxs-lookup"><span data-stu-id="28d4b-116">_int_</span></span> <br/> |<span data-ttu-id="28d4b-117">必須</span><span class="sxs-lookup"><span data-stu-id="28d4b-117">Required</span></span>  <br/> |<span data-ttu-id="28d4b-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="28d4b-118">**Integer**</span></span> <br/> |<span data-ttu-id="28d4b-p101">色の輝度を増加する量を指定します。正または負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="28d4b-p101">The amount by which to increase the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="28d4b-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="28d4b-121">Return value</span></span>

 <span data-ttu-id="28d4b-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="28d4b-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="28d4b-123">注釈</span><span class="sxs-lookup"><span data-stu-id="28d4b-123">Remarks</span></span>

<span data-ttu-id="28d4b-124">明度の上限と下限は、それぞれ 0 と 240 です。</span><span class="sxs-lookup"><span data-stu-id="28d4b-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="28d4b-125">_Int_パラメーターに渡すことができます、整数のサイズに制限はありませんが、明度がこの制限を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="28d4b-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  

