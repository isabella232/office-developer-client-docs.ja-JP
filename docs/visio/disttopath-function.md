---
title: DISTTOPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: 指定した座標で表される点からパス上の点までの最短距離を返します。
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332691"
---
# <a name="disttopath-function"></a><span data-ttu-id="66819-103">DISTTOPATH 関数</span><span class="sxs-lookup"><span data-stu-id="66819-103">DISTTOPATH Function</span></span>

<span data-ttu-id="66819-104">指定した座標で表される点からパス上の点までの最短距離を返します。</span><span class="sxs-lookup"><span data-stu-id="66819-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="66819-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="66819-105">Version Information</span></span>

<span data-ttu-id="66819-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="66819-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="66819-107">構文</span><span class="sxs-lookup"><span data-stu-id="66819-107">Syntax</span></span>

<span data-ttu-id="66819-108">disttopath (\* \* *section* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="66819-108">DISTTOPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="66819-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="66819-109">Parameters</span></span>

|<span data-ttu-id="66819-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="66819-110">**Name**</span></span>|<span data-ttu-id="66819-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="66819-111">**Required/Optional**</span></span>|<span data-ttu-id="66819-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="66819-112">**Data Type**</span></span>|<span data-ttu-id="66819-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="66819-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="66819-114">_セクション_</span><span class="sxs-lookup"><span data-stu-id="66819-114">_section_</span></span> <br/> |<span data-ttu-id="66819-115">必須</span><span class="sxs-lookup"><span data-stu-id="66819-115">Required</span></span>  <br/> |<span data-ttu-id="66819-116">**String**</span><span class="sxs-lookup"><span data-stu-id="66819-116">**String**</span></span> <br/> |<span data-ttu-id="66819-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="66819-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="66819-118">_x_</span><span class="sxs-lookup"><span data-stu-id="66819-118">_x_</span></span> <br/> |<span data-ttu-id="66819-119">必須</span><span class="sxs-lookup"><span data-stu-id="66819-119">Required</span></span>  <br/> |<span data-ttu-id="66819-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="66819-120">**Double**</span></span> <br/> |<span data-ttu-id="66819-121">点の_x_座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="66819-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="66819-122">_y_</span><span class="sxs-lookup"><span data-stu-id="66819-122">_y_</span></span> <br/> |<span data-ttu-id="66819-123">必須</span><span class="sxs-lookup"><span data-stu-id="66819-123">Required</span></span>  <br/> |<span data-ttu-id="66819-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="66819-124">**Double**</span></span> <br/> |<span data-ttu-id="66819-125">点の_y_座標です。</span><span class="sxs-lookup"><span data-stu-id="66819-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="66819-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="66819-126">Return value</span></span>

 <span data-ttu-id="66819-127">**倍精度浮動小数点型 (Double)**</span><span class="sxs-lookup"><span data-stu-id="66819-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="66819-128">解説</span><span class="sxs-lookup"><span data-stu-id="66819-128">Remarks</span></span>

<span data-ttu-id="66819-129">section が存在しない場合、#REF!</span><span class="sxs-lookup"><span data-stu-id="66819-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="66819-130">_セクション_が存在しない場合。</span><span class="sxs-lookup"><span data-stu-id="66819-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="66819-131">戻り値は、点がトラベルの方向の左側にある場合は正、右側にある場合は負になります。</span><span class="sxs-lookup"><span data-stu-id="66819-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

