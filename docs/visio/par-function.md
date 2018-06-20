---
title: PAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: 親図形の座標系の x、点の y 座標を返します。
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805975"
---
# <a name="par-function"></a><span data-ttu-id="e6a21-103">PAR 関数</span><span class="sxs-lookup"><span data-stu-id="e6a21-103">PAR Function</span></span>

<span data-ttu-id="e6a21-104">親図形の座標系の点の_x, y_座標を返します。</span><span class="sxs-lookup"><span data-stu-id="e6a21-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="e6a21-105">構文</span><span class="sxs-lookup"><span data-stu-id="e6a21-105">Syntax</span></span>

<span data-ttu-id="e6a21-106">額面価格 (* **ポイント** *)</span><span class="sxs-lookup"><span data-stu-id="e6a21-106">PAR(** *point* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="e6a21-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="e6a21-107">Parameters</span></span>

|<span data-ttu-id="e6a21-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="e6a21-108">**Name**</span></span>|<span data-ttu-id="e6a21-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="e6a21-109">**Required/Optional**</span></span>|<span data-ttu-id="e6a21-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="e6a21-110">**Data Type**</span></span>|<span data-ttu-id="e6a21-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="e6a21-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="e6a21-112">_ポイント_</span><span class="sxs-lookup"><span data-stu-id="e6a21-112">_point_</span></span> <br/> |<span data-ttu-id="e6a21-113">必須</span><span class="sxs-lookup"><span data-stu-id="e6a21-113">Required</span></span>  <br/> |<span data-ttu-id="e6a21-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="e6a21-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="e6a21-115">現在の図形の座標系にある点の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="e6a21-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e6a21-116">備考</span><span class="sxs-lookup"><span data-stu-id="e6a21-116">Remarks</span></span>

<span data-ttu-id="e6a21-117">Microsoft Visio で、ポイントは、 *x*および*y*のペアを具体化した単一の値の座標です。</span><span class="sxs-lookup"><span data-stu-id="e6a21-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="e6a21-118">図形がグループ内にある場合は、その親はグループです。</span><span class="sxs-lookup"><span data-stu-id="e6a21-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="e6a21-119">図形がグループ内にない場合は、その親はページです。</span><span class="sxs-lookup"><span data-stu-id="e6a21-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="e6a21-120">例</span><span class="sxs-lookup"><span data-stu-id="e6a21-120">Example</span></span>

<span data-ttu-id="e6a21-121">PAR(PNT(PinX,PinY))</span><span class="sxs-lookup"><span data-stu-id="e6a21-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="e6a21-p102">この式では、PNT 関数によって現在の図形内にある座標の組み合わせが点に変換されます。次に PAR によって、この点が、現在の図形を含んでいるページまたはグループの左下隅を基準にした座標の組み合わせに変換されます。</span><span class="sxs-lookup"><span data-stu-id="e6a21-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

