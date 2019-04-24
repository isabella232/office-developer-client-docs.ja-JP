---
title: POINTALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: パスの点またはパスからのオフセットの座標を返します。
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348259"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="82152-103">POINTALONGPATH 関数</span><span class="sxs-lookup"><span data-stu-id="82152-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="82152-104">パスの点またはパスからのオフセットの座標を返します。</span><span class="sxs-lookup"><span data-stu-id="82152-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="82152-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="82152-105">Version Information</span></span>

<span data-ttu-id="82152-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="82152-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="82152-107">構文</span><span class="sxs-lookup"><span data-stu-id="82152-107">Syntax</span></span>

<span data-ttu-id="82152-108">POINTALONGPATH (\* **セクション** *、* **トラベル** \* \* \* *[, offset]* \* \* \* \* *[, segment]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="82152-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="82152-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82152-109">Parameters</span></span>

|<span data-ttu-id="82152-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="82152-110">**Name**</span></span>|<span data-ttu-id="82152-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="82152-111">**Required/Optional**</span></span>|<span data-ttu-id="82152-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="82152-112">**Data Type**</span></span>|<span data-ttu-id="82152-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="82152-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="82152-114">_セクション_</span><span class="sxs-lookup"><span data-stu-id="82152-114">_section_</span></span> <br/> |<span data-ttu-id="82152-115">必須</span><span class="sxs-lookup"><span data-stu-id="82152-115">Required</span></span>  <br/> |<span data-ttu-id="82152-116">**String**</span><span class="sxs-lookup"><span data-stu-id="82152-116">**String**</span></span> <br/> |<span data-ttu-id="82152-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="82152-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="82152-118">_travel_</span><span class="sxs-lookup"><span data-stu-id="82152-118">_travel_</span></span> <br/> |<span data-ttu-id="82152-119">必須</span><span class="sxs-lookup"><span data-stu-id="82152-119">Required</span></span>  <br/> |<span data-ttu-id="82152-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="82152-120">**Double**</span></span> <br/> |<span data-ttu-id="82152-121">点を識別する、スキャンするパスの始点から終点までの割合。</span><span class="sxs-lookup"><span data-stu-id="82152-121">The percentage of the path traversed, from the begin point to the end point that identifies the point.</span></span> <span data-ttu-id="82152-122">0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82152-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="82152-123">_交互_</span><span class="sxs-lookup"><span data-stu-id="82152-123">_offset_</span></span> <br/> |<span data-ttu-id="82152-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="82152-124">Optional</span></span>  <br/> |<span data-ttu-id="82152-125">**倍精度浮動小数点型 (Double)**</span><span class="sxs-lookup"><span data-stu-id="82152-125">**Double**</span></span> <br/> |<span data-ttu-id="82152-126">点がパスからオフセットする距離。</span><span class="sxs-lookup"><span data-stu-id="82152-126">The distance that the point is offset from the path.</span></span> <span data-ttu-id="82152-127">詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="82152-127">See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="82152-128">_化_</span><span class="sxs-lookup"><span data-stu-id="82152-128">_segment_</span></span> <br/> |<span data-ttu-id="82152-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="82152-129">Optional</span></span>  <br/> |<span data-ttu-id="82152-130">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="82152-130">**Integer**</span></span> <br/> |<span data-ttu-id="82152-131">座標を計算するパスの 1 から始まるセグメント。</span><span class="sxs-lookup"><span data-stu-id="82152-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="82152-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="82152-132">Return value</span></span>

 <span data-ttu-id="82152-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="82152-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82152-134">解説</span><span class="sxs-lookup"><span data-stu-id="82152-134">Remarks</span></span>

<span data-ttu-id="82152-135">_セクション_または_セグメント_が存在しない場合は、#REF! が返されます。</span><span class="sxs-lookup"><span data-stu-id="82152-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="82152-136">正の*オフセット*値は、トラベルの方向の左側にある点を指定します。</span><span class="sxs-lookup"><span data-stu-id="82152-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="82152-137">負の*オフセット*値は、トラベル方向の右にある点を指定します。</span><span class="sxs-lookup"><span data-stu-id="82152-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="82152-138">**Point** は、図形座標 (*x,y*) の整列されたペアを 1 つの値として表します。</span><span class="sxs-lookup"><span data-stu-id="82152-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

