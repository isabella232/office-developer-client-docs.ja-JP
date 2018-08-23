---
title: PATHLENGTH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: 指定した [Geometry] セクションで定義されているパスの長さを返します。
ms.openlocfilehash: 37cabbde9fc0782bc1fde46f3065d0c945c9dada
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805981"
---
# <a name="pathlength-function"></a><span data-ttu-id="77e80-103">PATHLENGTH 関数</span><span class="sxs-lookup"><span data-stu-id="77e80-103">PATHLENGTH Function</span></span>

<span data-ttu-id="77e80-104">指定した [Geometry] セクションで定義されているパスの長さを返します。</span><span class="sxs-lookup"><span data-stu-id="77e80-104">Returns the length of the path that is defined in the specified Geometry section.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="77e80-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="77e80-105">Version Information</span></span>

<span data-ttu-id="77e80-106">追加バージョン: Visio 2010
</span><span class="sxs-lookup"><span data-stu-id="77e80-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="77e80-107">構文</span><span class="sxs-lookup"><span data-stu-id="77e80-107">Syntax</span></span>

<span data-ttu-id="77e80-108">PATHLENGTH (* **で** * * * *[] セグメント** *)</span><span class="sxs-lookup"><span data-stu-id="77e80-108">PATHLENGTH(** *section* ** ** *[,segment]* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="77e80-109">パラメーター</span><span class="sxs-lookup"><span data-stu-id="77e80-109">Parameters</span></span>

|<span data-ttu-id="77e80-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="77e80-110">**Name**</span></span>|<span data-ttu-id="77e80-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="77e80-111">**Required/Optional**</span></span>|<span data-ttu-id="77e80-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="77e80-112">**Data Type**</span></span>|<span data-ttu-id="77e80-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="77e80-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="77e80-114">_section_</span><span class="sxs-lookup"><span data-stu-id="77e80-114">_section_</span></span> <br/> |<span data-ttu-id="77e80-115">必須</span><span class="sxs-lookup"><span data-stu-id="77e80-115">Required</span></span>  <br/> |<span data-ttu-id="77e80-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="77e80-116">**String**</span></span> <br/> |<span data-ttu-id="77e80-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="77e80-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="77e80-118">_セグメント_</span><span class="sxs-lookup"><span data-stu-id="77e80-118">_segment_</span></span> <br/> |<span data-ttu-id="77e80-119">省略可能</span><span class="sxs-lookup"><span data-stu-id="77e80-119">Optional</span></span>  <br/> |<span data-ttu-id="77e80-120">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="77e80-120">**Integer**</span></span> <br/> |<span data-ttu-id="77e80-121">測定するパスの 1 から始まるセグメント。</span><span class="sxs-lookup"><span data-stu-id="77e80-121">The 1-based segment of the path to measure.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="77e80-122">戻り値</span><span class="sxs-lookup"><span data-stu-id="77e80-122">Return value</span></span>

 <span data-ttu-id="77e80-123">**Double**</span><span class="sxs-lookup"><span data-stu-id="77e80-123">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="77e80-124">注釈</span><span class="sxs-lookup"><span data-stu-id="77e80-124">Remarks</span></span>

<span data-ttu-id="77e80-125">_セクション_または_セグメント_が存在しない場合 Microsoft Visio は #ref! を返します。</span><span class="sxs-lookup"><span data-stu-id="77e80-125">If  _section_ or  _segment_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  
<span data-ttu-id="77e80-126">_セグメント_の値を含めると、PATHLENGTH はその部分だけの長さを返します。</span><span class="sxs-lookup"><span data-stu-id="77e80-126">If you include a  _segment_ value, PATHLENGTH returns the length of that segment only.</span></span> 
  

