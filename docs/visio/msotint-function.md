---
title: MSOTINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1bae0af9-229d-e114-4feb-bf6d7a7d8b08
description: 指定した割合で明度を増やして色を変更します。
ms.openlocfilehash: d63b90d0cd6fcb35e23a8efa4ca9e13e2838bc21
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335197"
---
# <a name="msotint-function"></a><span data-ttu-id="87dd7-103">MSOTINT 関数</span><span class="sxs-lookup"><span data-stu-id="87dd7-103">MSOTINT Function</span></span>

<span data-ttu-id="87dd7-104">指定した割合で明度を増やして色を変更します。</span><span class="sxs-lookup"><span data-stu-id="87dd7-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="87dd7-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="87dd7-105">Version Information</span></span>

<span data-ttu-id="87dd7-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="87dd7-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="87dd7-107">構文</span><span class="sxs-lookup"><span data-stu-id="87dd7-107">Syntax</span></span>

<span data-ttu-id="87dd7-108">msotint (\* \* *color* \* \*, \* \* *deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="87dd7-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="87dd7-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="87dd7-109">Parameters</span></span>

|<span data-ttu-id="87dd7-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="87dd7-110">**Name**</span></span>|<span data-ttu-id="87dd7-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="87dd7-111">**Required/Optional**</span></span>|<span data-ttu-id="87dd7-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="87dd7-112">**Data Type**</span></span>|<span data-ttu-id="87dd7-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="87dd7-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="87dd7-114">_color_</span><span class="sxs-lookup"><span data-stu-id="87dd7-114">_color_</span></span> <br/> |<span data-ttu-id="87dd7-115">必須</span><span class="sxs-lookup"><span data-stu-id="87dd7-115">Required</span></span>  <br/> |<span data-ttu-id="87dd7-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="87dd7-116">**RGB**</span></span> <br/> |<span data-ttu-id="87dd7-117">標準の RGB (red、green、blue) による色の値または色への参照。</span><span class="sxs-lookup"><span data-stu-id="87dd7-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="87dd7-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="87dd7-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="87dd7-119">必須</span><span class="sxs-lookup"><span data-stu-id="87dd7-119">Required</span></span>  <br/> |<span data-ttu-id="87dd7-120">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="87dd7-120">**Integer**</span></span> <br/> |<span data-ttu-id="87dd7-121">パーセンテージを白に変更します (-100%)または黒 (100%)_色_の値から。</span><span class="sxs-lookup"><span data-stu-id="87dd7-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87dd7-122">解説</span><span class="sxs-lookup"><span data-stu-id="87dd7-122">Remarks</span></span>

<span data-ttu-id="87dd7-123">_色_の値が白または黒に近いほど、特定の_deltaLum_値によって生成される濃淡に対する変更が小さくなります。</span><span class="sxs-lookup"><span data-stu-id="87dd7-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

