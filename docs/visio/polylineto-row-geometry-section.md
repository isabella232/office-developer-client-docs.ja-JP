---
title: '[PolylineTo] 行 ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251757
localization_priority: Normal
ms.assetid: b78a993f-4165-438d-39cf-9461b2877f17
description: ポリラインの最後の点とポリライン式の x 座標と y 座標を格納します。
ms.openlocfilehash: 13e5bd7138103094f0f00ad0512e33e9e6ad5e7f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359830"
---
# <a name="polylineto-row-geometry-section"></a>[PolylineTo] 行 ([Geometry] セクション)

ポリラインの最後の点とポリライン式の*x*座標と*y*座標を格納します。 
  
[PolylineTo] 行には次のセルが含まれます。
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |ポリラインの最後の頂点に対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |ポリラインの最後の頂点に対する*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |ポリラインの数式です。  <br/> |
   
## <a name="remarks"></a>解説

[Polyline] 行として表示される行は、一連の [LineTo] 行として表示される行と同じものです。ただし、[Polyline] 行の方が高機能です。図形の座標をより見やすくするために、[PolylineTo] 行から [LineTo] 行に変更することができます。これを行うには、[Polyline] 行を右クリックして、ショートカット メニューの **[行の拡張]** をクリックします。 
  
行の種類を [PolylineTo] 行に変更するには、行を右クリックして、ショートカット メニューの [**図形要素の変更**] をクリックします。 
  

