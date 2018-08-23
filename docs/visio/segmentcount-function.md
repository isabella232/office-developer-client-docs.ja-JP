---
title: SEGMENTCOUNT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 792ec0e4-4a48-136b-904c-fe269e355070
description: パスを形成する線分の数を返します。
ms.openlocfilehash: 93a77d9085e6900f502a75401847ad685d25effd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806376"
---
# <a name="segmentcount-function"></a><span data-ttu-id="73dfb-103">SEGMENTCOUNT 関数</span><span class="sxs-lookup"><span data-stu-id="73dfb-103">SEGMENTCOUNT Function</span></span>

<span data-ttu-id="73dfb-104">パスを形成する線分の数を返します。</span><span class="sxs-lookup"><span data-stu-id="73dfb-104">Returns the number of line segments that make up the path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="73dfb-105">構文</span><span class="sxs-lookup"><span data-stu-id="73dfb-105">Syntax</span></span>

<span data-ttu-id="73dfb-106">SEGMENTCOUNT (* * *pathRef* * *)</span><span class="sxs-lookup"><span data-stu-id="73dfb-106">SEGMENTCOUNT(** *pathRef* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="73dfb-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="73dfb-107">Parameters</span></span>

|<span data-ttu-id="73dfb-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="73dfb-108">**Name**</span></span>|<span data-ttu-id="73dfb-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="73dfb-109">**Required/Optional**</span></span>|<span data-ttu-id="73dfb-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="73dfb-110">**Data Type**</span></span>|<span data-ttu-id="73dfb-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="73dfb-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="73dfb-112">_pathRef_</span><span class="sxs-lookup"><span data-stu-id="73dfb-112">_pathRef_</span></span> <br/> |<span data-ttu-id="73dfb-113">必須</span><span class="sxs-lookup"><span data-stu-id="73dfb-113">Required</span></span>  <br/> |<span data-ttu-id="73dfb-114">**Integer**</span><span class="sxs-lookup"><span data-stu-id="73dfb-114">**Integer**</span></span> <br/> |<span data-ttu-id="73dfb-115">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="73dfb-115">The Geometry section that represents the path, specified by a reference to Path cell (for example, Geometry1.Path).</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="73dfb-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="73dfb-116">Return value</span></span>

<span data-ttu-id="73dfb-117">整数</span><span class="sxs-lookup"><span data-stu-id="73dfb-117">Integer</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73dfb-118">注釈</span><span class="sxs-lookup"><span data-stu-id="73dfb-118">Remarks</span></span>

<span data-ttu-id="73dfb-119">飛び越し点は、返される線分の合計数には含まれません。</span><span class="sxs-lookup"><span data-stu-id="73dfb-119">Line jumps are not included in the total number of segments returned.</span></span>
  

