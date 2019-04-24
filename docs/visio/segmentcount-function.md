---
title: SEGMENTCOUNT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: パスを形成する線分の数を返します。
ms.openlocfilehash: 947e37c13de638e4f281bc17376a253a8ca07e04
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326041"
---
# <a name="segmentcount-function"></a><span data-ttu-id="41826-103">SEGMENTCOUNT 関数</span><span class="sxs-lookup"><span data-stu-id="41826-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="41826-104">パスを形成する線分の数を返します。</span><span class="sxs-lookup"><span data-stu-id="41826-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="41826-105">構文</span><span class="sxs-lookup"><span data-stu-id="41826-105">Syntax</span></span>

<span data-ttu-id="41826-106">SEGMENTCOUNT (\* \* *pa f* \* \*)</span><span class="sxs-lookup"><span data-stu-id="41826-106">SEGMENTCOUNT(\*\* *pathRef* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="41826-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="41826-107">Parameters</span></span>

|<span data-ttu-id="41826-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="41826-108">**Name**</span></span>|<span data-ttu-id="41826-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="41826-109">**Required/Optional**</span></span>|<span data-ttu-id="41826-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="41826-110">**Data Type**</span></span>|<span data-ttu-id="41826-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="41826-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="41826-112">_paば f_</span><span class="sxs-lookup"><span data-stu-id="41826-112">_pathRef_</span></span> <br/> |<span data-ttu-id="41826-113">必須</span><span class="sxs-lookup"><span data-stu-id="41826-113">Required</span></span>  <br/> |<span data-ttu-id="41826-114">**整数型 (Integer)**</span><span class="sxs-lookup"><span data-stu-id="41826-114">**Integer**</span></span> <br/> |<span data-ttu-id="41826-115">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="41826-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="41826-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="41826-116">Return value</span></span>

<span data-ttu-id="41826-117">整数</span><span class="sxs-lookup"><span data-stu-id="41826-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41826-118">解説</span><span class="sxs-lookup"><span data-stu-id="41826-118">Remarks</span></span>

<span data-ttu-id="41826-119">飛び越し点は、返される線分の合計数には含まれません。</span><span class="sxs-lookup"><span data-stu-id="41826-119">Line jumps are not included in the total number of segments returned.</span></span>
  

