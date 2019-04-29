---
title: NEARESTPOINTONPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: 指定した座標に最も近い点のパスに沿った距離の割合を、0 ～ 1 の値として返します。
ms.openlocfilehash: ced20cdf1f3531eafaa03c2666b09334029fd3da
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407334"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="880bb-103">NEARESTPOINTONPATH 関数</span><span class="sxs-lookup"><span data-stu-id="880bb-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="880bb-104">指定した座標に最も近い点のパスに沿った距離の割合を、0 ～ 1 の値として返します。</span><span class="sxs-lookup"><span data-stu-id="880bb-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="880bb-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="880bb-105">Version Information</span></span>

<span data-ttu-id="880bb-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="880bb-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="880bb-107">構文</span><span class="sxs-lookup"><span data-stu-id="880bb-107">Syntax</span></span>

<span data-ttu-id="880bb-108">nearestpointonpath (\* \* *section* \* \*, \* \* *x* \* \*, \* \* *y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="880bb-108">NEARESTPOINTONPATH(\*\* *section* \*\*, \*\* *x* \*\*, \*\* *y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="880bb-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="880bb-109">Parameters</span></span>

|<span data-ttu-id="880bb-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="880bb-110">**Name**</span></span>|<span data-ttu-id="880bb-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="880bb-111">**Required/Optional**</span></span>|<span data-ttu-id="880bb-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="880bb-112">**Data Type**</span></span>|<span data-ttu-id="880bb-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="880bb-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="880bb-114">_セクション_</span><span class="sxs-lookup"><span data-stu-id="880bb-114">_section_</span></span> <br/> |<span data-ttu-id="880bb-115">必須</span><span class="sxs-lookup"><span data-stu-id="880bb-115">Required</span></span>  <br/> |<span data-ttu-id="880bb-116">**String**</span><span class="sxs-lookup"><span data-stu-id="880bb-116">**String**</span></span> <br/> |<span data-ttu-id="880bb-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="880bb-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="880bb-118">_x_</span><span class="sxs-lookup"><span data-stu-id="880bb-118">_x_</span></span> <br/> |<span data-ttu-id="880bb-119">必須</span><span class="sxs-lookup"><span data-stu-id="880bb-119">Required</span></span>  <br/> |<span data-ttu-id="880bb-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="880bb-120">**Double**</span></span> <br/> |<span data-ttu-id="880bb-121">指定した点の_x_座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="880bb-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="880bb-122">_y_</span><span class="sxs-lookup"><span data-stu-id="880bb-122">_y_</span></span> <br/> |<span data-ttu-id="880bb-123">必須</span><span class="sxs-lookup"><span data-stu-id="880bb-123">Required</span></span>  <br/> |<span data-ttu-id="880bb-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="880bb-124">**Double**</span></span> <br/> |<span data-ttu-id="880bb-125">指定した点の_y_座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="880bb-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="880bb-126">戻り値</span><span class="sxs-lookup"><span data-stu-id="880bb-126">Return value</span></span>

 <span data-ttu-id="880bb-127">**倍精度浮動小数点型 (Double)**</span><span class="sxs-lookup"><span data-stu-id="880bb-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="880bb-128">注釈</span><span class="sxs-lookup"><span data-stu-id="880bb-128">Remarks</span></span>

<span data-ttu-id="880bb-129">_section_が存在しない場合は、#REF を返します。</span><span class="sxs-lookup"><span data-stu-id="880bb-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

