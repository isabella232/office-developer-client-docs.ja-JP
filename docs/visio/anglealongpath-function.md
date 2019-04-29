---
title: ANGLEALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: 指定されたポイントのパスに対する接線の角度を返します。
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407327"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="44d95-103">ANGLEALONGPATH 関数</span><span class="sxs-lookup"><span data-stu-id="44d95-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="44d95-104">指定されたポイントのパスに対する接線の角度を返します。</span><span class="sxs-lookup"><span data-stu-id="44d95-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="44d95-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="44d95-105">Version Information</span></span>

<span data-ttu-id="44d95-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="44d95-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="44d95-107">構文</span><span class="sxs-lookup"><span data-stu-id="44d95-107">Syntax</span></span>

<span data-ttu-id="44d95-108">ANGLEALONGPATH (\* **セクション** *、* **トラベル** \* \* \* *[, segment]* \* \*)</span><span class="sxs-lookup"><span data-stu-id="44d95-108">ANGLEALONGPATH(\*\* *section* \*\*, \*\* *travel* \*\* \*\* *[,segment]* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="44d95-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="44d95-109">Parameters</span></span>

|<span data-ttu-id="44d95-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="44d95-110">**Name**</span></span>|<span data-ttu-id="44d95-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="44d95-111">**Required/Optional**</span></span>|<span data-ttu-id="44d95-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="44d95-112">**Data Type**</span></span>|<span data-ttu-id="44d95-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="44d95-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="44d95-114">_セクション_</span><span class="sxs-lookup"><span data-stu-id="44d95-114">_section_</span></span> <br/> |<span data-ttu-id="44d95-115">必須</span><span class="sxs-lookup"><span data-stu-id="44d95-115">Required</span></span>  <br/> |<span data-ttu-id="44d95-116">**String**</span><span class="sxs-lookup"><span data-stu-id="44d95-116">**String**</span></span> <br/> |<span data-ttu-id="44d95-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="44d95-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="44d95-118">_travel_</span><span class="sxs-lookup"><span data-stu-id="44d95-118">_travel_</span></span> <br/> |<span data-ttu-id="44d95-119">必須</span><span class="sxs-lookup"><span data-stu-id="44d95-119">Required</span></span>  <br/> |<span data-ttu-id="44d95-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="44d95-120">**Double**</span></span> <br/> |<span data-ttu-id="44d95-121">パスの始点から終点までの割合。</span><span class="sxs-lookup"><span data-stu-id="44d95-121">The percentage along the path from begin point to end point.</span></span> <span data-ttu-id="44d95-122">0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="44d95-122">Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="44d95-123">_化_</span><span class="sxs-lookup"><span data-stu-id="44d95-123">_segment_</span></span> <br/> |<span data-ttu-id="44d95-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="44d95-124">Optional</span></span>  <br/> |<span data-ttu-id="44d95-125">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="44d95-125">**Integer**</span></span> <br/> |<span data-ttu-id="44d95-126">接線角度を計算するパスの 1 から始まるセグメント。</span><span class="sxs-lookup"><span data-stu-id="44d95-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="44d95-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="44d95-127">Return value</span></span>

 <span data-ttu-id="44d95-128">**倍精度浮動小数点型 (Double)**</span><span class="sxs-lookup"><span data-stu-id="44d95-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="44d95-129">注釈</span><span class="sxs-lookup"><span data-stu-id="44d95-129">Remarks</span></span>

<span data-ttu-id="44d95-130">_セグメント_値を指定すると、ANGLEALONGPATH はそのセグメントの値のみを返します。</span><span class="sxs-lookup"><span data-stu-id="44d95-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="44d95-131">_セグメント_値を指定すると、ANGLEALONGPATH は、_トラベル_を使用して、_セグメント_に沿った segment を計算することで、正接の点を決定します。</span><span class="sxs-lookup"><span data-stu-id="44d95-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="44d95-132">_section_または_segment_のいずれかが存在しない場合は、#REF! が返されます。</span><span class="sxs-lookup"><span data-stu-id="44d95-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

