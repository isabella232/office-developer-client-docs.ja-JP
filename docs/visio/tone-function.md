---
title: TONE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: int パラメーターで指定された量で鮮やかさを小さくして、色を変更します。
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335687"
---
# <a name="tone-function"></a><span data-ttu-id="c838d-103">TONE 関数</span><span class="sxs-lookup"><span data-stu-id="c838d-103">TONE Function</span></span>

<span data-ttu-id="c838d-104">_int_パラメーターで指定された量で鮮やかさを小さくして、色を変更します。</span><span class="sxs-lookup"><span data-stu-id="c838d-104">Modifies the color by decreasing its saturation by the amount specified in the  _int_ parameter.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="c838d-105">構文</span><span class="sxs-lookup"><span data-stu-id="c838d-105">Syntax</span></span>

<span data-ttu-id="c838d-106">トーン (\* \* *color* \* *、* \* *int* \* \*)</span><span class="sxs-lookup"><span data-stu-id="c838d-106">TONE(\*\* *color* \*\*, \*\* *int* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c838d-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="c838d-107">Parameters</span></span>

|<span data-ttu-id="c838d-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="c838d-108">**Name**</span></span>|<span data-ttu-id="c838d-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="c838d-109">**Required/Optional**</span></span>|<span data-ttu-id="c838d-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="c838d-110">**Data Type**</span></span>|<span data-ttu-id="c838d-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="c838d-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c838d-112">_color_</span><span class="sxs-lookup"><span data-stu-id="c838d-112">_color_</span></span> <br/> |<span data-ttu-id="c838d-113">必須</span><span class="sxs-lookup"><span data-stu-id="c838d-113">Required</span></span>  <br/> |<span data-ttu-id="c838d-114">**数値型 (Numeric)**</span><span class="sxs-lookup"><span data-stu-id="c838d-114">**Numeric**</span></span> <br/> |<span data-ttu-id="c838d-115">Microsoft Visio カラー インデックスまたは RGB 値を指定します。</span><span class="sxs-lookup"><span data-stu-id="c838d-115">The Microsoft Visio color index or RGB value of the color.</span></span>  <br/> |
| <span data-ttu-id="c838d-116">_int_</span><span class="sxs-lookup"><span data-stu-id="c838d-116">_int_</span></span> <br/> |<span data-ttu-id="c838d-117">必須</span><span class="sxs-lookup"><span data-stu-id="c838d-117">Required</span></span>  <br/> |<span data-ttu-id="c838d-118">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="c838d-118">**Integer**</span></span> <br/> |<span data-ttu-id="c838d-119">色の鮮やかさを減少する量を指定します。</span><span class="sxs-lookup"><span data-stu-id="c838d-119">The amount by which to decrease the saturation of the color.</span></span> <span data-ttu-id="c838d-120">正または負の値を指定できます。</span><span class="sxs-lookup"><span data-stu-id="c838d-120">Can be positive or negative.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="c838d-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="c838d-121">Return value</span></span>

 <span data-ttu-id="c838d-122">**RGB**</span><span class="sxs-lookup"><span data-stu-id="c838d-122">**RGB**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c838d-123">解説</span><span class="sxs-lookup"><span data-stu-id="c838d-123">Remarks</span></span>

<span data-ttu-id="c838d-124">鮮やかさの上限と下限はそれぞれ 0 と 240 です。</span><span class="sxs-lookup"><span data-stu-id="c838d-124">The upper and lower limits of saturation are 0 and 240 respectively.</span></span> <span data-ttu-id="c838d-125">_int_パラメーターに渡すことができる整数のサイズに制限はありませんが、鮮やかさがこれらの制限を超えることはありません。</span><span class="sxs-lookup"><span data-stu-id="c838d-125">There is no limit on the size of the integer you can pass for the  _int_ parameter, but saturation never exceeds these limits.</span></span> 
  

