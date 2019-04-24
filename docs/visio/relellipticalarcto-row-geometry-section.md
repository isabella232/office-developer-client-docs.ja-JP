---
title: '[RelEllipticalArcTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: 図形の幅と高さを基準にした楕円弧の端点の x 座標および y 座標、図形の幅と高さに相対する円弧のコントロールポイントの x 座標と y 座標、x 軸から楕円の長軸までの角度、および t 間の比率を格納します。楕円の長軸と短軸。
ms.openlocfilehash: e38f5f2baf6bb9ade31c2778799a3ece968147f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359963"
---
# <a name="relellipticalarcto-row-geometry-section"></a>[RelEllipticalArcTo] 行 ([図形座標] セクション)

図形** の幅と高さに相対する楕円の弧の端点に対する x 座標と*y*座標、図形の幅と高さに相対する円弧のコントロールポイントの*x*座標および*y*座標、および*x*からの角度を含みます。  -楕円の主軸までの軸、および楕円の長軸と短軸との比率を示します。 
  
> [!NOTE]
> [**RelEllipticalArcTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 Visio 2003-2010 形式でファイルを保存すると、 **[relellipticalarcto]** 行は[[ellipticalarcto]](ellipticalarcto-row-geometry-section.md)の行に変換されます。 
  
[**RelEllipticalArcTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形の幅を基準にして、円弧の最後の頂点に対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形の高さを基準にして、円弧の最後の頂点に対する*y*座標です。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |図形の幅を基準にした円弧のコントロールポイントの*x*座標です。弧の点を指定します。コントロールポイントは、円弧の始点と終点の間の中間点を中心に配置されます。それ以外の場合、円弧はコントロールポイントを通過するために極端なサイズまで拡大することがあり、予期しない結果が発生することがあります。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |図形の幅を基準にした円弧のコントロールポイントの*y*座標です。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |親の*x*軸を基準にした円弧の主軸の角度。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
   
## <a name="remarks"></a>解説

[**RelEllipticalArcTo**] 行の値は、図形の幅と高さを乗算した [[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)] 行の値に等しくなります。 例: **X**、 **Y**、 **a**、 **B**、 **C**、および**D**の各セルが値1、1、1.5、0.5、15 deg、1.5 (それぞれ) を持つ **[relellipticalarcto]** 行は、 **[ellipticalarcto]** の行で置き換えることができます。セル数式`Width*1`、 `Height*1'`、 `Width*1.5` `Height*0.5`、、15 deg、および 1.5 (それぞれ)。
  

