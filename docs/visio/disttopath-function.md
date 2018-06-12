---
title: DISTTOPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: 指定した座標で表される点からパス上の点までの最短距離を返します。
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805255"
---
# <a name="disttopath-function"></a><span data-ttu-id="19ba5-103">DISTTOPATH 関数</span><span class="sxs-lookup"><span data-stu-id="19ba5-103">DISTTOPATH Function</span></span>

<span data-ttu-id="19ba5-104">指定した座標で表される点からパス上の点までの最短距離を返します。</span><span class="sxs-lookup"><span data-stu-id="19ba5-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="19ba5-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="19ba5-105">Version Information</span></span>

<span data-ttu-id="19ba5-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="19ba5-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="19ba5-107">構文</span><span class="sxs-lookup"><span data-stu-id="19ba5-107">Syntax</span></span>

<span data-ttu-id="19ba5-108">DISTTOPATH (* **で** *、* * *x* * *、* * *y* * *)</span><span class="sxs-lookup"><span data-stu-id="19ba5-108">DISTTOPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="19ba5-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="19ba5-109">Parameters</span></span>

|<span data-ttu-id="19ba5-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="19ba5-110">**Name**</span></span>|<span data-ttu-id="19ba5-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="19ba5-111">**Required/Optional**</span></span>|<span data-ttu-id="19ba5-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="19ba5-112">**Data Type**</span></span>|<span data-ttu-id="19ba5-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="19ba5-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="19ba5-114">_section_</span><span class="sxs-lookup"><span data-stu-id="19ba5-114">_section_</span></span> <br/> |<span data-ttu-id="19ba5-115">必須</span><span class="sxs-lookup"><span data-stu-id="19ba5-115">Required</span></span>  <br/> |<span data-ttu-id="19ba5-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="19ba5-116">**String**</span></span> <br/> |<span data-ttu-id="19ba5-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="19ba5-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="19ba5-118">_x_</span><span class="sxs-lookup"><span data-stu-id="19ba5-118">_x_</span></span> <br/> |<span data-ttu-id="19ba5-119">必須</span><span class="sxs-lookup"><span data-stu-id="19ba5-119">Required</span></span>  <br/> |<span data-ttu-id="19ba5-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="19ba5-120">**Double**</span></span> <br/> |<span data-ttu-id="19ba5-121">_X_-点の座標です。</span><span class="sxs-lookup"><span data-stu-id="19ba5-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="19ba5-122">_y_</span><span class="sxs-lookup"><span data-stu-id="19ba5-122">_y_</span></span> <br/> |<span data-ttu-id="19ba5-123">必須</span><span class="sxs-lookup"><span data-stu-id="19ba5-123">Required</span></span>  <br/> |<span data-ttu-id="19ba5-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="19ba5-124">**Double**</span></span> <br/> |<span data-ttu-id="19ba5-125">_Y_-点の座標です。</span><span class="sxs-lookup"><span data-stu-id="19ba5-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="19ba5-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="19ba5-126">Return value</span></span>

 <span data-ttu-id="19ba5-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="19ba5-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="19ba5-128">解説</span><span class="sxs-lookup"><span data-stu-id="19ba5-128">Remarks</span></span>

<span data-ttu-id="19ba5-129">Microsoft Visio では、#REF を返す!</span><span class="sxs-lookup"><span data-stu-id="19ba5-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="19ba5-130">_セクション_が存在しません。 場合、</span><span class="sxs-lookup"><span data-stu-id="19ba5-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="19ba5-131">戻り値は、点がトラベルの方向の左側にある場合は正、右側にある場合は負になります。</span><span class="sxs-lookup"><span data-stu-id="19ba5-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

