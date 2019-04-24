---
title: PATHSEGMENT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 08accf3b-93ac-9dd3-85ce-34ad42e79a4f
description: 指定したパーセント記号に沿った、指定されたパスにある1から始まるセグメント番号を返します。
ms.openlocfilehash: c4dfc4d33de1a9c1a03ef14d76103b4de0f28bc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344451"
---
# <a name="pathsegment-function"></a><span data-ttu-id="eb0ff-103">PATHSEGMENT 関数</span><span class="sxs-lookup"><span data-stu-id="eb0ff-103">PATHSEGMENT Function</span></span>

<span data-ttu-id="eb0ff-104">指定したパーセント記号に沿った、指定されたパスにある1から始まるセグメント番号を返します。</span><span class="sxs-lookup"><span data-stu-id="eb0ff-104">Returns the 1-based segment number at the specified percentage mark along the specified path.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="eb0ff-105">構文</span><span class="sxs-lookup"><span data-stu-id="eb0ff-105">Syntax</span></span>

<span data-ttu-id="eb0ff-106">pathsegment (\* **セクション** *、* **トラベル** \*)</span><span class="sxs-lookup"><span data-stu-id="eb0ff-106">PATHSEGMENT(\*\* *section* \*\*, \*\* *travel* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="eb0ff-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="eb0ff-107">Parameters</span></span>

|<span data-ttu-id="eb0ff-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-108">**Name**</span></span>|<span data-ttu-id="eb0ff-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-109">**Required/Optional**</span></span>|<span data-ttu-id="eb0ff-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-110">**Data Type**</span></span>|<span data-ttu-id="eb0ff-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="eb0ff-112">_セクション_</span><span class="sxs-lookup"><span data-stu-id="eb0ff-112">_section_</span></span> <br/> |<span data-ttu-id="eb0ff-113">必須</span><span class="sxs-lookup"><span data-stu-id="eb0ff-113">Required</span></span>  <br/> |<span data-ttu-id="eb0ff-114">**String**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-114">**String**</span></span> <br/> |<span data-ttu-id="eb0ff-115">パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。</span><span class="sxs-lookup"><span data-stu-id="eb0ff-115">The Geometry section that represents the path, specified by a reference to its Path cell (for example, Geometry1.Path).</span></span>  <br/> |
| <span data-ttu-id="eb0ff-116">_travel_</span><span class="sxs-lookup"><span data-stu-id="eb0ff-116">_travel_</span></span> <br/> |<span data-ttu-id="eb0ff-117">必須</span><span class="sxs-lookup"><span data-stu-id="eb0ff-117">Required</span></span>  <br/> |<span data-ttu-id="eb0ff-118">**Double**</span><span class="sxs-lookup"><span data-stu-id="eb0ff-118">**Double**</span></span> <br/> |<span data-ttu-id="eb0ff-119">スキャンするパスの始点から終点までの割合。</span><span class="sxs-lookup"><span data-stu-id="eb0ff-119">The percentage of the path traversed, from the begin point to the end point.</span></span> <span data-ttu-id="eb0ff-120">0 ～ 1 の値を指定する必要があります。</span><span class="sxs-lookup"><span data-stu-id="eb0ff-120">Must be between 0 and 1.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="eb0ff-121">戻り値</span><span class="sxs-lookup"><span data-stu-id="eb0ff-121">Return value</span></span>

<span data-ttu-id="eb0ff-122">整数型 (Integer)</span><span class="sxs-lookup"><span data-stu-id="eb0ff-122">Integer</span></span>
  

