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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406424"
---
# <a name="msotint-function"></a><span data-ttu-id="84286-103">MSOTINT 関数</span><span class="sxs-lookup"><span data-stu-id="84286-103">MSOTINT Function</span></span>

<span data-ttu-id="84286-104">指定した割合で明度を増やして色を変更します。</span><span class="sxs-lookup"><span data-stu-id="84286-104">Modifies the color by increasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="84286-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="84286-105">Version Information</span></span>

<span data-ttu-id="84286-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="84286-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="84286-107">構文</span><span class="sxs-lookup"><span data-stu-id="84286-107">Syntax</span></span>

<span data-ttu-id="84286-108">msotint (\* \* *color* \* \*, \* \* *deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="84286-108">MSOTINT(\*\* *color* \*\*, \*\* *deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="84286-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="84286-109">Parameters</span></span>

|<span data-ttu-id="84286-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="84286-110">**Name**</span></span>|<span data-ttu-id="84286-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="84286-111">**Required/Optional**</span></span>|<span data-ttu-id="84286-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="84286-112">**Data Type**</span></span>|<span data-ttu-id="84286-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="84286-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="84286-114">_color_</span><span class="sxs-lookup"><span data-stu-id="84286-114">_color_</span></span> <br/> |<span data-ttu-id="84286-115">必須</span><span class="sxs-lookup"><span data-stu-id="84286-115">Required</span></span>  <br/> |<span data-ttu-id="84286-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="84286-116">**RGB**</span></span> <br/> |<span data-ttu-id="84286-117">標準の RGB (red、green、blue) による色の値または色への参照。</span><span class="sxs-lookup"><span data-stu-id="84286-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="84286-118">_deltaLum_</span><span class="sxs-lookup"><span data-stu-id="84286-118">_deltaLum_</span></span> <br/> |<span data-ttu-id="84286-119">必須</span><span class="sxs-lookup"><span data-stu-id="84286-119">Required</span></span>  <br/> |<span data-ttu-id="84286-120">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="84286-120">**Integer**</span></span> <br/> |<span data-ttu-id="84286-121">パーセンテージを白に変更します (-100%)または黒 (100%)_色_の値から。</span><span class="sxs-lookup"><span data-stu-id="84286-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="84286-122">注釈</span><span class="sxs-lookup"><span data-stu-id="84286-122">Remarks</span></span>

<span data-ttu-id="84286-123">_色_の値が白または黒に近いほど、特定の_deltaLum_値によって生成される濃淡に対する変更が小さくなります。</span><span class="sxs-lookup"><span data-stu-id="84286-123">The closer the  _color_ value is to white or black, the smaller the change to the tint that is produced by a specific  _deltaLum_ value.</span></span> 
  

