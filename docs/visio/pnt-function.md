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
description: 座標で表される点を返します。 x および y 値を 1 つにします。
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806065"
---
# <a name="pnt-function"></a><span data-ttu-id="f032e-103">PNT 関数</span><span class="sxs-lookup"><span data-stu-id="f032e-103">PNT Function</span></span>

<span data-ttu-id="f032e-104">座標_x_と_y_を 1 つの値で表される点を返します。</span><span class="sxs-lookup"><span data-stu-id="f032e-104">Returns the point represented by the coordinates  _x_ and  _y_ as a single value.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="f032e-105">構文</span><span class="sxs-lookup"><span data-stu-id="f032e-105">Syntax</span></span>

<span data-ttu-id="f032e-106">Pnt 関数 (* * *x y* * *)</span><span class="sxs-lookup"><span data-stu-id="f032e-106">PNT(** *x,y* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="f032e-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="f032e-107">Parameters</span></span>

|<span data-ttu-id="f032e-108">**名前**</span><span class="sxs-lookup"><span data-stu-id="f032e-108">**Name**</span></span>|<span data-ttu-id="f032e-109">**必須 / オプション**</span><span class="sxs-lookup"><span data-stu-id="f032e-109">**Required/Optional**</span></span>|<span data-ttu-id="f032e-110">**データ型**</span><span class="sxs-lookup"><span data-stu-id="f032e-110">**Data Type**</span></span>|<span data-ttu-id="f032e-111">**説明**</span><span class="sxs-lookup"><span data-stu-id="f032e-111">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="f032e-112">_x, y_</span><span class="sxs-lookup"><span data-stu-id="f032e-112">_x,y_</span></span> <br/> |<span data-ttu-id="f032e-113">必須</span><span class="sxs-lookup"><span data-stu-id="f032e-113">Required</span></span>  <br/> |<span data-ttu-id="f032e-114">**番号**</span><span class="sxs-lookup"><span data-stu-id="f032e-114">**Number, Number**</span></span> <br/> |<span data-ttu-id="f032e-115">現在の図形の座標系にある点の座標を指定します。</span><span class="sxs-lookup"><span data-stu-id="f032e-115">The coordinates of the point in the coordinate system of the current shape.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="f032e-116">�߂�l</span><span class="sxs-lookup"><span data-stu-id="f032e-116">Return value</span></span>

<span data-ttu-id="f032e-117">点</span><span class="sxs-lookup"><span data-stu-id="f032e-117">Point</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f032e-118">注釈</span><span class="sxs-lookup"><span data-stu-id="f032e-118">Remarks</span></span>

<span data-ttu-id="f032e-119">ポイントに座標を変換すると、 *x*および*y*を操作しなくても図形座標を変更するのには、座標を別々 にします。</span><span class="sxs-lookup"><span data-stu-id="f032e-119">Converting coordinates to points allows you to change a shape's geometry without having to manipulate  *x*  - and  *y*  -coordinates separately.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f032e-120">例</span><span class="sxs-lookup"><span data-stu-id="f032e-120">Example</span></span>

<span data-ttu-id="f032e-121">PNT(PinX,PinY)</span><span class="sxs-lookup"><span data-stu-id="f032e-121">PNT(PinX,PinY)</span></span> 
  
<span data-ttu-id="f032e-122">[PinX] と [PinY] で表される点を返します。</span><span class="sxs-lookup"><span data-stu-id="f032e-122">Returns the point represented by PinX and PinY.</span></span> 
  

