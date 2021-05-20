---
title: ANGLEALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: 指定されたポイントのパスに対する接線の角度を返します。
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160294"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="76ec3-103">ANGLEALONGPATH 関数</span><span class="sxs-lookup"><span data-stu-id="76ec3-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="76ec3-104">指定されたポイントのパスに対する接線の角度を返します。</span><span class="sxs-lookup"><span data-stu-id="76ec3-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="76ec3-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="76ec3-105">Version Information</span></span>

<span data-ttu-id="76ec3-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="76ec3-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="76ec3-107">構文</span><span class="sxs-lookup"><span data-stu-id="76ec3-107">Syntax</span></span>

<span data-ttu-id="76ec3-108">ANGLEALONGPATH(***セクション***, ***travel*** ***[,segment]*** )</span><span class="sxs-lookup"><span data-stu-id="76ec3-108">ANGLEALONGPATH(***section***, ***travel*** ***[,segment]*** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="76ec3-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="76ec3-109">Parameters</span></span>

|<span data-ttu-id="76ec3-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="76ec3-110">**Name**</span></span>|<span data-ttu-id="76ec3-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="76ec3-111">**Required/Optional**</span></span>|<span data-ttu-id="76ec3-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="76ec3-112">**Data Type**</span></span>|<span data-ttu-id="76ec3-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="76ec3-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="76ec3-114">_セクション_</span><span class="sxs-lookup"><span data-stu-id="76ec3-114">_section_</span></span> <br/> |<span data-ttu-id="76ec3-115">必須</span><span class="sxs-lookup"><span data-stu-id="76ec3-115">Required</span></span>  <br/> |<span data-ttu-id="76ec3-116">**String**</span><span class="sxs-lookup"><span data-stu-id="76ec3-116">**String**</span></span> <br/> |<span data-ttu-id="76ec3-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="76ec3-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="76ec3-118">_旅行_</span><span class="sxs-lookup"><span data-stu-id="76ec3-118">_travel_</span></span> <br/> |<span data-ttu-id="76ec3-119">必須</span><span class="sxs-lookup"><span data-stu-id="76ec3-119">Required</span></span>  <br/> |<span data-ttu-id="76ec3-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="76ec3-120">**Double**</span></span> <br/> |<span data-ttu-id="76ec3-p101">パスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="76ec3-p101">The percentage along the path from begin point to end point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="76ec3-123">_segment_</span><span class="sxs-lookup"><span data-stu-id="76ec3-123">_segment_</span></span> <br/> |<span data-ttu-id="76ec3-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="76ec3-124">Optional</span></span>  <br/> |<span data-ttu-id="76ec3-125">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="76ec3-125">**Integer**</span></span> <br/> |<span data-ttu-id="76ec3-126">接線角度を計算するパスの 1 から始まるセグメント。</span><span class="sxs-lookup"><span data-stu-id="76ec3-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="76ec3-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="76ec3-127">Return value</span></span>

 <span data-ttu-id="76ec3-128">**倍精度浮動小数点型 (Double)**</span><span class="sxs-lookup"><span data-stu-id="76ec3-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="76ec3-129">注釈</span><span class="sxs-lookup"><span data-stu-id="76ec3-129">Remarks</span></span>

<span data-ttu-id="76ec3-130">セグメント値を含  _める場合_ 、ANGLEALONGPATH は、そのセグメントの値のみを返します。</span><span class="sxs-lookup"><span data-stu-id="76ec3-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="76ec3-131">セグメント値を含 _める場合_、ANGLEALONGPATH は、セグメントに沿ったパーサータージュを計算するために移動を使用して接線のポイントを決定 _します_。</span><span class="sxs-lookup"><span data-stu-id="76ec3-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="76ec3-132">セクションまたは _セグメント_ が _存在_ しない場合は、Microsoft Visio返#REF!。</span><span class="sxs-lookup"><span data-stu-id="76ec3-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

