---
title: PNT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: 座標 x と y によって表される点を、1つの値として返します。
ms.openlocfilehash: c0a12aa18f4c766ea1f5b0fa1d827804d766713c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322352"
---
# <a name="pnt-function"></a><span data-ttu-id="6a6ad-103">PNT 関数</span><span class="sxs-lookup"><span data-stu-id="6a6ad-103">PNT Function</span></span>

<span data-ttu-id="6a6ad-104">座標_x_と_y_によって表される点を、1つの値として返します。</span><span class="sxs-lookup"><span data-stu-id="6a6ad-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="6a6ad-105">構文</span><span class="sxs-lookup"><span data-stu-id="6a6ad-105">Syntax</span></span>

<span data-ttu-id="6a6ad-106">PNT (\* \* *x, y* \* \*)</span><span class="sxs-lookup"><span data-stu-id="6a6ad-106">PNT(\*\* *x,y* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="6a6ad-107">パラメーター</span><span class="sxs-lookup"><span data-stu-id="6a6ad-107">Parameters</span></span>

|<span data-ttu-id="6a6ad-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="6a6ad-108">**Name**</span></span>|<span data-ttu-id="6a6ad-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="6a6ad-109">**Required/Optional**</span></span>|<span data-ttu-id="6a6ad-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="6a6ad-110">**Data Type**</span></span>|<span data-ttu-id="6a6ad-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="6a6ad-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="6a6ad-112">_x、y_</span><span class="sxs-lookup"><span data-stu-id="6a6ad-112">_x,y_</span></span> <br/> |<span data-ttu-id="6a6ad-113">必須</span><span class="sxs-lookup"><span data-stu-id="6a6ad-113">Required</span></span>  <br/> |<span data-ttu-id="6a6ad-114">**数値型 (Number),数値型 (Number)**</span><span class="sxs-lookup"><span data-stu-id="6a6ad-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="6a6ad-115">現在の図形の座標系にある点の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="6a6ad-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="6a6ad-116">戻り値</span><span class="sxs-lookup"><span data-stu-id="6a6ad-116">Return value</span></span>

<span data-ttu-id="6a6ad-117">Point</span><span class="sxs-lookup"><span data-stu-id="6a6ad-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="6a6ad-118">解説</span><span class="sxs-lookup"><span data-stu-id="6a6ad-118">Remarks</span></span>

<span data-ttu-id="6a6ad-119">座標をポイントに変換すると、 *x*座標と*y*座標を個別に操作しなくても図形の座標を変更できます。</span><span class="sxs-lookup"><span data-stu-id="6a6ad-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="6a6ad-120">例</span><span class="sxs-lookup"><span data-stu-id="6a6ad-120">Example</span></span>

<span data-ttu-id="6a6ad-121">PNT (PinX、PinY)</span><span class="sxs-lookup"><span data-stu-id="6a6ad-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="6a6ad-122">[PinX] と [PinY] で表される点を返します。</span><span class="sxs-lookup"><span data-stu-id="6a6ad-122">Returns the point represented by PinX and PinY.</span></span> 
  

