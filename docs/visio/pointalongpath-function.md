---
title: POINTALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: パスの点またはパスからのオフセットの座標を返します。
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806021"
---
# <a name="pointalongpath-function"></a><span data-ttu-id="3c8d1-103">POINTALONGPATH 関数</span><span class="sxs-lookup"><span data-stu-id="3c8d1-103">POINTALONGPATH Function</span></span>

<span data-ttu-id="3c8d1-104">パスの点またはパスからのオフセットの座標を返します。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-104">Returns the coordinates of a point on, or offset from, the path.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="3c8d1-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="3c8d1-105">Version Information</span></span>

<span data-ttu-id="3c8d1-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="3c8d1-107">構文</span><span class="sxs-lookup"><span data-stu-id="3c8d1-107">Syntax</span></span>

<span data-ttu-id="3c8d1-108">POINTALONGPATH (* **で** *、* **旅行** * * * *[] オフセット** * * * *[] セグメント** *)</span><span class="sxs-lookup"><span data-stu-id="3c8d1-108">POINTALONGPATH(** *section* **, ** *travel* ** ** *[,offset]* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="3c8d1-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="3c8d1-109">Parameters</span></span>

|<span data-ttu-id="3c8d1-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-110">**Name**</span></span>|<span data-ttu-id="3c8d1-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-111">**Required/Optional**</span></span>|<span data-ttu-id="3c8d1-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-112">**Data Type**</span></span>|<span data-ttu-id="3c8d1-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="3c8d1-114">_section_</span><span class="sxs-lookup"><span data-stu-id="3c8d1-114">_section_</span></span> <br/> |<span data-ttu-id="3c8d1-115">必須</span><span class="sxs-lookup"><span data-stu-id="3c8d1-115">Required</span></span>  <br/> |<span data-ttu-id="3c8d1-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-116">**String**</span></span> <br/> |<span data-ttu-id="3c8d1-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="3c8d1-118">_旅行_</span><span class="sxs-lookup"><span data-stu-id="3c8d1-118">_travel_</span></span> <br/> |<span data-ttu-id="3c8d1-119">必須</span><span class="sxs-lookup"><span data-stu-id="3c8d1-119">Required</span></span>  <br/> |<span data-ttu-id="3c8d1-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-120">**Double**</span></span> <br/> |<span data-ttu-id="3c8d1-p101">点を識別する、スキャンするパスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-p101">The percentage of the path traversed, from the begin point to the end point that identifies the point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="3c8d1-123">_オフセット_</span><span class="sxs-lookup"><span data-stu-id="3c8d1-123">_offset_</span></span> <br/> |<span data-ttu-id="3c8d1-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c8d1-124">Optional</span></span>  <br/> |<span data-ttu-id="3c8d1-125">**倍精度浮動小数点型 (Double)**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-125">**Double**</span></span> <br/> |<span data-ttu-id="3c8d1-p102">点がパスからオフセットする距離。詳細については、「備考」を参照してください。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-p102">The distance that the point is offset from the path. See Remarks for more information.</span></span>  <br/> |
| <span data-ttu-id="3c8d1-128">_セグメント_</span><span class="sxs-lookup"><span data-stu-id="3c8d1-128">_segment_</span></span> <br/> |<span data-ttu-id="3c8d1-129">省略可能</span><span class="sxs-lookup"><span data-stu-id="3c8d1-129">Optional</span></span>  <br/> |<span data-ttu-id="3c8d1-130">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-130">**Integer**</span></span> <br/> |<span data-ttu-id="3c8d1-131">座標を計算するパスの 1 から始まるセグメント。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-131">The 1-based segment of the path in which to calculate the coordinates.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="3c8d1-132">�߂�l</span><span class="sxs-lookup"><span data-stu-id="3c8d1-132">Return value</span></span>

 <span data-ttu-id="3c8d1-133">**ポイント**</span><span class="sxs-lookup"><span data-stu-id="3c8d1-133">**Point**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3c8d1-134">Remarks</span><span class="sxs-lookup"><span data-stu-id="3c8d1-134">Remarks</span></span>

<span data-ttu-id="3c8d1-135">_セクション_または_セグメント_が存在しない場合 Microsoft Visio は #ref! を返します。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-135">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="3c8d1-136">正の*オフセット*値では、旅行の方向の左へのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-136">Positive  *offset*  values specify points to the left of the direction of travel.</span></span> 
  
<span data-ttu-id="3c8d1-137">負の*オフセット*値では、旅行の方向の右へのポインターを指定します。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-137">Negative  *offset*  values specify points to the right of the direction of travel.</span></span> 
  
<span data-ttu-id="3c8d1-138">**ポイント**は、1 つの値としての幾何学の座標 (*x, y*) 座標ペアを表します。</span><span class="sxs-lookup"><span data-stu-id="3c8d1-138">A **Point** represents an ordered pair of geometric coordinates (*x,y*) as a single value.</span></span> 
  

