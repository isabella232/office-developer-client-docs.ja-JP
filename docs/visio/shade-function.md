---
title: SHADE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b4fbcb8-1ae4-c9fb-6337-b72f49aedd91
description: Int パラメーターで指定した量 (正または負) によって明度を下げて、色を変更します。
ms.openlocfilehash: 4a02aa41050c3cf36b567c238670b5f61074bd7c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806379"
---
# <a name="shade-function"></a><span data-ttu-id="0db14-103">SHADE 関数</span><span class="sxs-lookup"><span data-stu-id="0db14-103">SHADE Function</span></span>

<span data-ttu-id="0db14-104">_Int_パラメーターで指定した量 (正または負) によって明度を下げて、色を変更します。</span><span class="sxs-lookup"><span data-stu-id="0db14-104">Modifies the color by decreasing its luminosity by the amount (positive or negative) specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="0db14-105">構文</span><span class="sxs-lookup"><span data-stu-id="0db14-105">Syntax</span></span>

<span data-ttu-id="0db14-106">網掛け (* **色** *、* * *int* * *)</span><span class="sxs-lookup"><span data-stu-id="0db14-106">SHADE(** *color* **, ** *int* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="0db14-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="0db14-107">Parameters</span></span>

|<span data-ttu-id="0db14-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="0db14-108">**Name**</span></span>|<span data-ttu-id="0db14-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="0db14-109">**Required/Optional**</span></span>|<span data-ttu-id="0db14-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="0db14-110">**Data Type**</span></span>|<span data-ttu-id="0db14-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="0db14-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="0db14-112">_color_</span><span class="sxs-lookup"><span data-stu-id="0db14-112">_color_</span></span> <br/> |<span data-ttu-id="0db14-113">必須</span><span class="sxs-lookup"><span data-stu-id="0db14-113">Required</span></span>  <br/> |<span data-ttu-id="0db14-114">**数値**</span><span class="sxs-lookup"><span data-stu-id="0db14-114">**Numeric**</span></span> <br/> |<span data-ttu-id="0db14-115">Microsoft Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="0db14-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="0db14-116">_int_</span><span class="sxs-lookup"><span data-stu-id="0db14-116">_int_</span></span> <br/> |<span data-ttu-id="0db14-117">必須</span><span class="sxs-lookup"><span data-stu-id="0db14-117">Required</span></span>  <br/> |<span data-ttu-id="0db14-118">**Integer**</span><span class="sxs-lookup"><span data-stu-id="0db14-118">**Integer**</span></span> <br/> |<span data-ttu-id="0db14-p101">色の輝度を減少する量を指定します。正または負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="0db14-p101">The amount by which to decrease the luminosity of the color. Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="0db14-121">�߂�l</span><span class="sxs-lookup"><span data-stu-id="0db14-121">Return value</span></span>

 <span data-ttu-id="0db14-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="0db14-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0db14-123">備考</span><span class="sxs-lookup"><span data-stu-id="0db14-123">Remarks</span></span>

<span data-ttu-id="0db14-124">明度の上限と下限は、それぞれ 0 と 240 です。</span><span class="sxs-lookup"><span data-stu-id="0db14-124">The upper and lower limits of luminosity are 0 and 240 respectively.</span></span> <span data-ttu-id="0db14-125">_Int_パラメーターに渡すことができます、整数のサイズに制限はありませんが、明度がこの制限を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="0db14-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but luminosity never exceeds these limits.</span></span> 
  
![](media/image199_ZA10173627.gif)
  

