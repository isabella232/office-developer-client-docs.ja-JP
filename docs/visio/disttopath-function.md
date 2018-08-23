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
# <a name="disttopath-function"></a><span data-ttu-id="aeaf9-103">DISTTOPATH 関数</span><span class="sxs-lookup"><span data-stu-id="aeaf9-103">DISTTOPATH Function</span></span>

<span data-ttu-id="aeaf9-104">指定した座標で表される点からパス上の点までの最短距離を返します。</span><span class="sxs-lookup"><span data-stu-id="aeaf9-104">Returns the shortest distance from the point represented by the specified coordinates to a point on the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="aeaf9-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="aeaf9-105">Version Information</span></span>

<span data-ttu-id="aeaf9-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="aeaf9-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="aeaf9-107">構文</span><span class="sxs-lookup"><span data-stu-id="aeaf9-107">Syntax</span></span>

<span data-ttu-id="aeaf9-108">DISTTOPATH (* **で** *、* * *x* * *、* * *y* * *)</span><span class="sxs-lookup"><span data-stu-id="aeaf9-108">DISTTOPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="aeaf9-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="aeaf9-109">Parameters</span></span>

|<span data-ttu-id="aeaf9-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-110">**Name**</span></span>|<span data-ttu-id="aeaf9-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-111">**Required/Optional**</span></span>|<span data-ttu-id="aeaf9-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-112">**Data Type**</span></span>|<span data-ttu-id="aeaf9-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="aeaf9-114">_section_</span><span class="sxs-lookup"><span data-stu-id="aeaf9-114">_section_</span></span> <br/> |<span data-ttu-id="aeaf9-115">必須</span><span class="sxs-lookup"><span data-stu-id="aeaf9-115">Required</span></span>  <br/> |<span data-ttu-id="aeaf9-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-116">**String**</span></span> <br/> |<span data-ttu-id="aeaf9-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="aeaf9-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="aeaf9-118">_x_</span><span class="sxs-lookup"><span data-stu-id="aeaf9-118">_x_</span></span> <br/> |<span data-ttu-id="aeaf9-119">必須</span><span class="sxs-lookup"><span data-stu-id="aeaf9-119">Required</span></span>  <br/> |<span data-ttu-id="aeaf9-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-120">**Double**</span></span> <br/> |<span data-ttu-id="aeaf9-121">_X_-点の座標です。</span><span class="sxs-lookup"><span data-stu-id="aeaf9-121">The  _x_-coordinate of the point.</span></span>  <br/> |
| <span data-ttu-id="aeaf9-122">_y_</span><span class="sxs-lookup"><span data-stu-id="aeaf9-122">_y_</span></span> <br/> |<span data-ttu-id="aeaf9-123">必須</span><span class="sxs-lookup"><span data-stu-id="aeaf9-123">Required</span></span>  <br/> |<span data-ttu-id="aeaf9-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-124">**Double**</span></span> <br/> |<span data-ttu-id="aeaf9-125">_Y_-点の座標です。</span><span class="sxs-lookup"><span data-stu-id="aeaf9-125">The  _y_-coordinate of the point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="aeaf9-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="aeaf9-126">Return value</span></span>

 <span data-ttu-id="aeaf9-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="aeaf9-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="aeaf9-128">注釈</span><span class="sxs-lookup"><span data-stu-id="aeaf9-128">Remarks</span></span>

<span data-ttu-id="aeaf9-129">Microsoft Visio では、#REF を返す!</span><span class="sxs-lookup"><span data-stu-id="aeaf9-129">Microsoft Visio returns #REF!</span></span> <span data-ttu-id="aeaf9-130">_セクション_が存在しません。 場合、</span><span class="sxs-lookup"><span data-stu-id="aeaf9-130">if  _section_ does not exist.</span></span> 
  
<span data-ttu-id="aeaf9-131">戻り値は、点がトラベルの方向の左側にある場合は正、右側にある場合は負になります。</span><span class="sxs-lookup"><span data-stu-id="aeaf9-131">The returned value is positive if the point is to the left of the direction of travel; it is negative if the point is to the right of the direction of travel.</span></span>
  

