---
title: ANGLEALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: 指定されたポイントのパスに対する接線の角度を返します。
ms.openlocfilehash: ec5529037275fc8661972cc7403886cd33150b38
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804797"
---
# <a name="anglealongpath-function"></a><span data-ttu-id="82441-103">ANGLEALONGPATH 関数</span><span class="sxs-lookup"><span data-stu-id="82441-103">ANGLEALONGPATH Function</span></span>

<span data-ttu-id="82441-104">指定されたポイントのパスに対する接線の角度を返します。</span><span class="sxs-lookup"><span data-stu-id="82441-104">Returns the angle of the tangent to the path at a given point.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="82441-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="82441-105">Version Information</span></span>

<span data-ttu-id="82441-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="82441-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="82441-107">構文</span><span class="sxs-lookup"><span data-stu-id="82441-107">Syntax</span></span>

<span data-ttu-id="82441-108">ANGLEALONGPATH (* **で** *、* **旅行** * * * *[] セグメント** *)</span><span class="sxs-lookup"><span data-stu-id="82441-108">ANGLEALONGPATH(** *section* **, ** *travel* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="82441-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="82441-109">Parameters</span></span>

|<span data-ttu-id="82441-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="82441-110">**Name**</span></span>|<span data-ttu-id="82441-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="82441-111">**Required/Optional**</span></span>|<span data-ttu-id="82441-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="82441-112">**Data Type**</span></span>|<span data-ttu-id="82441-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="82441-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="82441-114">_section_</span><span class="sxs-lookup"><span data-stu-id="82441-114">_section_</span></span> <br/> |<span data-ttu-id="82441-115">必須</span><span class="sxs-lookup"><span data-stu-id="82441-115">Required</span></span>  <br/> |<span data-ttu-id="82441-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="82441-116">**String**</span></span> <br/> |<span data-ttu-id="82441-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="82441-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="82441-118">_旅行_</span><span class="sxs-lookup"><span data-stu-id="82441-118">_travel_</span></span> <br/> |<span data-ttu-id="82441-119">必須</span><span class="sxs-lookup"><span data-stu-id="82441-119">Required</span></span>  <br/> |<span data-ttu-id="82441-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="82441-120">**Double**</span></span> <br/> |<span data-ttu-id="82441-p101">パスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="82441-p101">The percentage along the path from begin point to end point. Must be between 0 and 1.</span></span>  <br/> |
| <span data-ttu-id="82441-123">_セグメント_</span><span class="sxs-lookup"><span data-stu-id="82441-123">_segment_</span></span> <br/> |<span data-ttu-id="82441-124">省略可能</span><span class="sxs-lookup"><span data-stu-id="82441-124">Optional</span></span>  <br/> |<span data-ttu-id="82441-125">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="82441-125">**Integer**</span></span> <br/> |<span data-ttu-id="82441-126">接線角度を計算するパスの 1 から始まるセグメント。</span><span class="sxs-lookup"><span data-stu-id="82441-126">The 1-based segment of the path at which to calculate the tangent angle.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="82441-127">戻り値</span><span class="sxs-lookup"><span data-stu-id="82441-127">Return value</span></span>

 <span data-ttu-id="82441-128">**Double**</span><span class="sxs-lookup"><span data-stu-id="82441-128">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="82441-129">注釈</span><span class="sxs-lookup"><span data-stu-id="82441-129">Remarks</span></span>

<span data-ttu-id="82441-130">_セグメント_の値を含めると、ANGLEALONGPATH はそのセグメントのみの値を返します。</span><span class="sxs-lookup"><span data-stu-id="82441-130">If you include a  _segment_ value, ANGLEALONGPATH returns the value for that segment only.</span></span> 
  
<span data-ttu-id="82441-131">_セグメント_の値を含めると、ANGLEALONGPATH は_旅行_を使用して_セグメント_に沿って percertage を計算するのには、接線の点を決定します。</span><span class="sxs-lookup"><span data-stu-id="82441-131">If you include a  _segment_ value, ANGLEALONGPATH determines the point of the tangent by using  _travel_ to calculate the percertage along  _segment_.</span></span>
  
<span data-ttu-id="82441-132">_セクション_または_セグメント_のいずれかが存在しない場合 Microsoft Visio は #ref! を返します。</span><span class="sxs-lookup"><span data-stu-id="82441-132">If either  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

