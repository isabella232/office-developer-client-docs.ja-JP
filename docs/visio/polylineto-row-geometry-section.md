---
title: '[PolylineTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
ms.localizationpriority: medium
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: ポリラインの最後の点の x 座標と y 座標、およびポリライン数式を含む。
ms.openlocfilehash: bd4456109bfd313d67e4778d73b92b9335a99d13
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608047"
---
# <a name="polylineto-row-geometry-section"></a>[PolylineTo] 行 ([Geometry] セクション)

ポリラインの  *最後*  の点の x 座標と  *y*  座標、およびポリライン数式を含む。 
  
[PolylineTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |ポリライン  *の*  終了頂点の x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |ポリライン  *の終了*  頂点の y 座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |ポリラインの数式です。  <br/> |
   
## <a name="remarks"></a>注釈

[Polyline] 行として表示される行は、一連の [LineTo] 行として表示される行と同じものです。ただし、[Polyline] 行の方が高機能です。図形の座標をより見やすくするために、[PolylineTo] 行から [LineTo] 行に変更することができます。これを行うには、[Polyline] 行を右クリックして、ショートカット メニューの **[行の拡張]** をクリックします。 
  
行の種類を [PolylineTo] 行に変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。 
  

