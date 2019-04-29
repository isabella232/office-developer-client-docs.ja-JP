---
title: '[InfiniteLine] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3020
localization_priority: Normal
ms.assetid: 55942a42-5e88-2f6b-69f8-405ce406fcaf
description: 無限線上にある2つの点の x 座標と y 座標を格納します。
ms.openlocfilehash: b6338b6b50535379759649c791b9678de640df70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413620"
---
# <a name="infiniteline-row-geometry-section"></a>[InfiniteLine] 行 ([Geometry] セクション)

無限線上にある2つの点の*x*座標と*y*座標を格納します。 
  
[InfiniteLine] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |無限線上の点の*x*座標です。対応する** y 座標は [y セルで表されます。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |無限線上の点の*y*座標です。対応する*x*座標は [x」セルで表されます。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |無限線上の点の*x*座標です。対応する*y*座標は [B セルで表されます。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |無限線上の点の*y*座標です。対応する*x*座標は、A セルで表されます。  <br/> |
   
## <a name="remarks"></a>注釈

[Ellipse] 行または [InfiniteLine] 行を含む [Geometry] セクションには、他の行を入れることができません。
  

