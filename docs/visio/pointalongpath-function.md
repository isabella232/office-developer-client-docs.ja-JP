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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430484"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="a2341-103">POINTALONGPATH 関数</span><span class="sxs-lookup"><span data-stu-id="a2341-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="a2341-104">パスの点またはパスからのオフセットの座標を返します。</span><span class="sxs-lookup"><span data-stu-id="a2341-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="a2341-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="a2341-105">Version Information</span></span>

<span data-ttu-id="a2341-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="a2341-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a2341-107">構文</span><span class="sxs-lookup"><span data-stu-id="a2341-107">Syntax</span></span>

<span data-ttu-id="a2341-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span><span class="sxs-lookup"><span data-stu-id="a2341-108">POINTALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,offset]* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a2341-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="a2341-109">Parameters</span></span>

|<span data-ttu-id="a2341-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="a2341-110">**Name**</span></span>|<span data-ttu-id="a2341-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="a2341-111">**Required/Optional**</span></span>|<span data-ttu-id="a2341-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="a2341-112">**Data Type**</span></span>|<span data-ttu-id="a2341-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="a2341-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a2341-114">_セクション_</span><span class="sxs-lookup"><span data-stu-id="a2341-114">_section_</span></span> <br/> |<span data-ttu-id="a2341-115">必須</span><span class="sxs-lookup"><span data-stu-id="a2341-115">Required</span></span>  <br/> |<span data-ttu-id="a2341-116">**String**</span><span class="sxs-lookup"><span data-stu-id="a2341-116">**String**</span></span> <br/> |<span data-ttu-id="a2341-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="a2341-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="a2341-118">_旅行_</span><span class="sxs-lookup"><span data-stu-id="a2341-118">_travel_</span></span> <br/> |<span data-ttu-id="a2341-119">必須</span><span class="sxs-lookup"><span data-stu-id="a2341-119">Required</span></span>  <br/> |<span data-ttu-id="a2341-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="a2341-120">**Double**</span></span> <br/> |<span data-ttu-id="a2341-p101">点を識別する、スキャンするパスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="a2341-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="a2341-123">_offset_</span><span class="sxs-lookup"><span data-stu-id="a2341-123">_offset_</span></span> <br/> |<span data-ttu-id="a2341-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="a2341-124">Optional</span></span>  <br/> |<span data-ttu-id="a2341-125">**倍精度浮動小数点型 (Double)**</span><span class="sxs-lookup"><span data-stu-id="a2341-125">**Double**</span></span> <br/> |<span data-ttu-id="a2341-p102">点がパスからオフセットする距離。詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="a2341-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="a2341-128">_segment_</span><span class="sxs-lookup"><span data-stu-id="a2341-128">_segment_</span></span> <br/> |<span data-ttu-id="a2341-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="a2341-129">Optional</span></span>  <br/> |<span data-ttu-id="a2341-130">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="a2341-130">**Integer**</span></span> <br/> |<span data-ttu-id="a2341-131">座標を計算するパスの 1 から始まるセグメント。</span><span class="sxs-lookup"><span data-stu-id="a2341-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a2341-132">戻り値</span><span class="sxs-lookup"><span data-stu-id="a2341-132">Return value</span></span>

 <span data-ttu-id="a2341-133">**Point**</span><span class="sxs-lookup"><span data-stu-id="a2341-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a2341-134">注釈</span><span class="sxs-lookup"><span data-stu-id="a2341-134">Remarks</span></span>

<span data-ttu-id="a2341-135">セクション _または_ セグメント _が存在_ しない場合、Microsoft Visioが#REF!</span><span class="sxs-lookup"><span data-stu-id="a2341-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="a2341-136">正  *のオフセット*  値は、移動方向の左側のポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="a2341-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="a2341-137">負  *のオフセット*  値は、移動方向の右側のポイントを指定します。</span><span class="sxs-lookup"><span data-stu-id="a2341-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="a2341-138">**Point** は、図形座標 (*x,y*) の整列されたペアを 1 つの値として表します。</span><span class="sxs-lookup"><span data-stu-id="a2341-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

