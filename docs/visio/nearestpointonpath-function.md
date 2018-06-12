---
title: NEARESTPOINTONPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: 指定した座標に最も近い点のパスに沿った距離の割合を、0 ～ 1 の値として返します。
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805912"
---
# <a name="nearestpointonpath-function"></a><span data-ttu-id="e0446-103">NEARESTPOINTONPATH 関数</span><span class="sxs-lookup"><span data-stu-id="e0446-103">NEARESTPOINTONPATH Function</span></span>

<span data-ttu-id="e0446-104">指定した座標に最も近い点のパスに沿った距離の割合を、0 ～ 1 の値として返します。</span><span class="sxs-lookup"><span data-stu-id="e0446-104">Returns the percentage of the distance along the path of the point that is nearest to the specified coordinates, as a value between 0 and 1.</span></span>
  
## <a name="version-information"></a><span data-ttu-id="e0446-105">バージョン情報</span><span class="sxs-lookup"><span data-stu-id="e0446-105">Version Information</span></span>

<span data-ttu-id="e0446-106">Visio 2010 のバージョンが追加されます。</span><span class="sxs-lookup"><span data-stu-id="e0446-106">Version Added: Visio 2010</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e0446-107">構文</span><span class="sxs-lookup"><span data-stu-id="e0446-107">Syntax</span></span>

<span data-ttu-id="e0446-108">NEARESTPOINTONPATH (* **で** *、* * *x* * *、* * *y* * *)</span><span class="sxs-lookup"><span data-stu-id="e0446-108">NEARESTPOINTONPATH(** *section* **, ** *x* **, ** *y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e0446-109">Parameters</span><span class="sxs-lookup"><span data-stu-id="e0446-109">Parameters</span></span>

|<span data-ttu-id="e0446-110">**名前**</span><span class="sxs-lookup"><span data-stu-id="e0446-110">**Name**</span></span>|<span data-ttu-id="e0446-111">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e0446-111">**Required/Optional**</span></span>|<span data-ttu-id="e0446-112">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e0446-112">**Data Type**</span></span>|<span data-ttu-id="e0446-113">**説明**</span><span class="sxs-lookup"><span data-stu-id="e0446-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e0446-114">_section_</span><span class="sxs-lookup"><span data-stu-id="e0446-114">_section_</span></span> <br/> |<span data-ttu-id="e0446-115">必須</span><span class="sxs-lookup"><span data-stu-id="e0446-115">Required</span></span>  <br/> |<span data-ttu-id="e0446-116">**文字列型 (String)**</span><span class="sxs-lookup"><span data-stu-id="e0446-116">**String**</span></span> <br/> |<span data-ttu-id="e0446-117">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="e0446-117">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="e0446-118">_x_</span><span class="sxs-lookup"><span data-stu-id="e0446-118">_x_</span></span> <br/> |<span data-ttu-id="e0446-119">必須</span><span class="sxs-lookup"><span data-stu-id="e0446-119">Required</span></span>  <br/> |<span data-ttu-id="e0446-120">**Double**</span><span class="sxs-lookup"><span data-stu-id="e0446-120">**Double**</span></span> <br/> |<span data-ttu-id="e0446-121">_X_で指定された点の座標です。</span><span class="sxs-lookup"><span data-stu-id="e0446-121">The  _x_-coordinate of the specified point.</span></span>  <br/> |
| <span data-ttu-id="e0446-122">_y_</span><span class="sxs-lookup"><span data-stu-id="e0446-122">_y_</span></span> <br/> |<span data-ttu-id="e0446-123">必須</span><span class="sxs-lookup"><span data-stu-id="e0446-123">Required</span></span>  <br/> |<span data-ttu-id="e0446-124">**Double**</span><span class="sxs-lookup"><span data-stu-id="e0446-124">**Double**</span></span> <br/> |<span data-ttu-id="e0446-125">_Y_で指定された点の座標です。</span><span class="sxs-lookup"><span data-stu-id="e0446-125">The  _y_-coordinate of the specified point.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="e0446-126">�߂�l</span><span class="sxs-lookup"><span data-stu-id="e0446-126">Return value</span></span>

 <span data-ttu-id="e0446-127">**Double**</span><span class="sxs-lookup"><span data-stu-id="e0446-127">**Double**</span></span>
  
## <a name="remarks"></a><span data-ttu-id="e0446-128">解説</span><span class="sxs-lookup"><span data-stu-id="e0446-128">Remarks</span></span>

<span data-ttu-id="e0446-129">_セクション_が存在しない場合 Microsoft Visio は #ref! を返します。</span><span class="sxs-lookup"><span data-stu-id="e0446-129">If  _section_ does not exist, Microsoft Visio returns #REF!.</span></span> 
  

