---
title: MSOSHADE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 905cd1cc-14d3-5d37-89c4-f8461a03dda2
description: 指定された割合で明度を減らして色を変更します。
ms.openlocfilehash: 207893552c7378589d4a648bf29ed88fcfd15224
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283711"
---
# <a name="msoshade-function"></a><span data-ttu-id="af498-103">MSOSHADE 関数</span><span class="sxs-lookup"><span data-stu-id="af498-103">MSOSHADE Function</span></span>

<span data-ttu-id="af498-104">指定された割合で明度を減らして色を変更します。</span><span class="sxs-lookup"><span data-stu-id="af498-104">Modifies the color by decreasing its luminosity by the specified percentage.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="af498-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="af498-105">Version Information</span></span>

<span data-ttu-id="af498-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="af498-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="af498-107">構文</span><span class="sxs-lookup"><span data-stu-id="af498-107">Syntax</span></span>

<span data-ttu-id="af498-108">msoshade (\* \* *color* \* \*, \* \* *-deltaLum* \* \*)</span><span class="sxs-lookup"><span data-stu-id="af498-108">MSOSHADE(\*\* *color* \*\*, \*\* *-deltaLum* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="af498-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="af498-109">Parameters</span></span>

|<span data-ttu-id="af498-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="af498-110">**Name**</span></span>|<span data-ttu-id="af498-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="af498-111">**Required/Optional**</span></span>|<span data-ttu-id="af498-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="af498-112">**Data Type**</span></span>|<span data-ttu-id="af498-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="af498-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="af498-114">_color_</span><span class="sxs-lookup"><span data-stu-id="af498-114">_color_</span></span> <br/> |<span data-ttu-id="af498-115">必須</span><span class="sxs-lookup"><span data-stu-id="af498-115">Required</span></span>  <br/> |<span data-ttu-id="af498-116">**RGB**</span><span class="sxs-lookup"><span data-stu-id="af498-116">**RGB**</span></span> <br/> |<span data-ttu-id="af498-117">標準の RGB (red、green、blue) による色の値または色への参照。</span><span class="sxs-lookup"><span data-stu-id="af498-117">The standard RGB (red, green, blue) color value or reference to a color.</span></span>  <br/> |
| <span data-ttu-id="af498-118">_-deltaLum_</span><span class="sxs-lookup"><span data-stu-id="af498-118">_-deltaLum_</span></span> <br/> |<span data-ttu-id="af498-119">必須</span><span class="sxs-lookup"><span data-stu-id="af498-119">Required</span></span>  <br/> |<span data-ttu-id="af498-120">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="af498-120">**Integer**</span></span> <br/> |<span data-ttu-id="af498-121">パーセンテージを白に変更します (-100%)または黒 (100%)_色_の値から。</span><span class="sxs-lookup"><span data-stu-id="af498-121">The percentage change toward white (-100%) or black (100%) from the  _color_ value.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="af498-122">解説</span><span class="sxs-lookup"><span data-stu-id="af498-122">Remarks</span></span>

<span data-ttu-id="af498-123">_色_の値が白または黒に近いほど、 _deltaLum_の値によって生成される網掛けの変化が小さくなります。</span><span class="sxs-lookup"><span data-stu-id="af498-123">The closer the  _color_ value is to white or black, the smaller the change to the shade that is produced by a specific  _-deltaLum_ value.</span></span> 
  

