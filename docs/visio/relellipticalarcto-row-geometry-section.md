---
title: '[RelEllipticalArcTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b7da082-5e55-411d-b109-7fb6fa8f6e8e
description: 図形の幅と高さに対する楕円円弧の端点の x 座標と y 座標、図形の幅と高さに対する円弧上のコントロール ポイントの x 座標と y 座標、x 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。
ms.openlocfilehash: ce97c531e199acc74c0b3581dcf24e72dbf2899b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607823"
---
# <a name="relellipticalarcto-row-geometry-section"></a>[RelEllipticalArcTo] 行 ([図形座標] セクション)

図形の幅と高さに対する楕円円弧の端点の x 座標と y 座標、図形の幅と高さに対する円弧上のコントロール ポイントの x 座標と *y* 座標 *、x* 軸から楕円の長軸への角度、楕円の長軸と短軸の比率を含む。  
  
> [!NOTE]
> [**RelEllipticalArcTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 ファイルを 2003 から 2010 の Visio 形式に保存すると **、RelEllipticalArcTo** 行は、エリプティカル [ArcTo](ellipticalarcto-row-geometry-section.md)行に変換されます。 
  
[**RelEllipticalArcTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形  *の*  幅を基準にした円弧上の終了頂点の x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形  *の高*  さを基準にした円弧上の終了頂点の y 座標。  <br/> |
|[A](a-cell-geometry-section.md) <br/> |図形  *の*  幅を基準にした円弧のコントロール ポイントの x 座標。円弧上のポイント。コントロール ポイントは、円弧の開始頂点と終了頂点の約半分の位置に最適です。それ以外の場合、コントロール ポイントを通過するために極端なサイズにアークが大きくなる可能性があります。予期しない結果が得られます。  <br/> |
|[B](b-cell-geometry-section.md) <br/> |図形  *の幅*  に対する円弧のコントロール ポイントの y 座標。  <br/> |
|[C](c-cell-geometry-section.md) <br/> |親の x 軸に対する円弧の長軸の角度。  <br/> |
|[D](d-cell-geometry-section.md) <br/> |円弧の長軸と短軸の比率です。これらの言葉の通常の意味とは関係なく、"長" 軸が "短" 軸よりも長い必要はありません。したがって、比率は 1 より大きい必要はありません。このセルを 0 以下、または 1000 より大きく設定すると、予測できない結果になる可能性があります。  <br/> |
   
## <a name="remarks"></a>注釈

[**RelEllipticalArcTo**] 行の値は、図形の幅と高さを乗算した [[EllipticalArcTo](ellipticalarcto-row-geometry-section.md)] 行の値に等しくなります。 たとえば、X、Y、A、B、C、および **D** セルの値が1、1、1.5、0.5、15 deg、および 1.5 (それぞれ) の **RelEllipticalArcTo** 行を、セル式 `Width*1` `Height*1'` `Width*1.5` `Height*0.5` 、15 deg、および 1.5 (それぞれ) のセル式で、1.5 に置き換えることができます。
  

