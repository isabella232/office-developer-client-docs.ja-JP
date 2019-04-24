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
description: 図形の親の座標系にある点の x, y 座標を返します。
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269945"
---
# <a name="par-function"></a><span data-ttu-id="d394e-103">PAR 関数</span><span class="sxs-lookup"><span data-stu-id="d394e-103">PAR Function</span></span>

<span data-ttu-id="d394e-104">図形の親の座標系にある点の_x, y_座標を返します。</span><span class="sxs-lookup"><span data-stu-id="d394e-104">Returns the  _x,y_ coordinates of a point in the coordinate system of the shape's parent.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="d394e-105">構文</span><span class="sxs-lookup"><span data-stu-id="d394e-105">Syntax</span></span>

<span data-ttu-id="d394e-106">額面 (\* **ポイント** \*)</span><span class="sxs-lookup"><span data-stu-id="d394e-106">PAR(\*\* *point* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d394e-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="d394e-107">Parameters</span></span>

|<span data-ttu-id="d394e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="d394e-108">**Name**</span></span>|<span data-ttu-id="d394e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="d394e-109">**Required/Optional**</span></span>|<span data-ttu-id="d394e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="d394e-110">**Data Type**</span></span>|<span data-ttu-id="d394e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="d394e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d394e-112">_ポイント_</span><span class="sxs-lookup"><span data-stu-id="d394e-112">_point_</span></span> <br/> |<span data-ttu-id="d394e-113">必須</span><span class="sxs-lookup"><span data-stu-id="d394e-113">Required</span></span>  <br/> |<span data-ttu-id="d394e-114">**数値型 (Number),数値型 (Number)**</span><span class="sxs-lookup"><span data-stu-id="d394e-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="d394e-115">現在の図形の座標系にある点の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="d394e-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d394e-116">解説</span><span class="sxs-lookup"><span data-stu-id="d394e-116">Remarks</span></span>

<span data-ttu-id="d394e-117">Microsoft Visio では、1つのポイントは*x*座標と*y*座標のペアを具体化した単一の値です。</span><span class="sxs-lookup"><span data-stu-id="d394e-117">In Microsoft Visio, a point is a single value that embodies a pair of  *x*  - and  *y*  -coordinates.</span></span> <span data-ttu-id="d394e-118">図形がグループに含まれる場合、その親はグループになります。</span><span class="sxs-lookup"><span data-stu-id="d394e-118">If the shape is in a group, its parent is the group.</span></span> <span data-ttu-id="d394e-119">図形がグループに含まれない場合、その親はページになります。</span><span class="sxs-lookup"><span data-stu-id="d394e-119">If the shape is not in a group, its parent is the page.</span></span> 
  
## <a name="example"></a><span data-ttu-id="d394e-120">例</span><span class="sxs-lookup"><span data-stu-id="d394e-120">Example</span></span>

<span data-ttu-id="d394e-121">額面 (PNT (PinX、PinY))</span><span class="sxs-lookup"><span data-stu-id="d394e-121">PAR(PNT(PinX,PinY))</span></span> 
  
<span data-ttu-id="d394e-p102">この式では、PNT 関数によって現在の図形内にある座標の組み合わせが点に変換されます。次に PAR によって、この点が、現在の図形を含んでいるページまたはグループの左下隅を基準にした座標の組み合わせに変換されます。</span><span class="sxs-lookup"><span data-stu-id="d394e-p102">In this expression, PNT converts a pair of coordinates in the current shape into a point. PAR then converts the point into a pair of coordinates in relation to the lower-left corner of the page or group that contains the current shape.</span></span> 
  

