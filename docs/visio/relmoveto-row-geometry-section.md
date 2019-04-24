---
title: '[RelMoveTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: 図形の最初の頂点に対する x 座標と y 座標、またはパスを切断した後の最初の頂点に対する x 座標と y 座標を格納します。これには、図形の高さと幅を基準にします。
ms.openlocfilehash: 488945dbeeea177514770da57b5f26ac947053a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319923"
---
# <a name="relmoveto-row-geometry-section"></a>[RelMoveTo] 行 ([図形座標] セクション)

図形の最初の頂点に対する*x*座標と*y*座標、またはパスを切断した後の最初の頂点に対する*x*座標と*y*座標を格納します。これには、図形の高さと幅を基準にします。 
  
> [!NOTE]
> [**RelMoveTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 Visio 2003-2010 形式でファイルを保存すると、[ **relmoveto** ] 行が [ [moveto](moveto-row-geometry-section.md) ] 行に変換されます。 
  
[**RelMoveTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |[ **relmoveto** ] 行がセクションの最初の行の場合、[x] セルは図形の幅を基準にして、図形の最初の頂点に対する*x*座標を表します。 2つの行の間に [ **relmoveto** ] 行が表示されている場合、[x] セルは、パスを切断した後の最初の頂点に対する*x*座標を表します。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |[ **relmoveto** ] 行がセクションの最初の行の場合、[y] セルは、図形の最初の頂点に対する*y*座標を表します。 2つの行の間に [ **relmoveto** ] 行が表示されている場合、[y] セルは、パスを切断した後の最初の頂点に対する*y*座標を表します。  <br/> |
   
## <a name="remarks"></a>解説

[**RelMoveTo**] 行の値は、図形の幅と高さを乗算した [[MoveTo](moveto-row-geometry-section.md)] 行の値に等しくなります。 例: [ **x** ] セルの値が "0" で、[ **y** ] セルの値が "0.5" の場合、[ **x** ] セルの値が数式 "Width **** 0" で、[ **** * **y** ] セルが数式である [moveto] 行に置き換えることができます。数式 "Height*0.5." 
  
[ **relmoveto** ] 行には、[moveto] 行がセクションの最初の行である場合に、図形の最初の頂点に対する*x*座標と*y*座標が含まれます。 通常、これは図形が描画されたときに最初に配置される頂点で、1-d 図形の始点には必ずしも対応していません。 
  
**Geometry**セクションは、[ **moveto** ] 行または [ **relmoveto** ] 行で開始する必要がありますが、図形の幅と高さに対する図形のパスの塗りつぶしのギャップを表すには、[ **relmoveto** ] 行と [ **moveto** ] 行を使用することもできます。 ただし、パスを使用して塗りつぶされた領域の境界を定義すると、このギャップは直線セグメントとして解釈されます。 このような隙間を挿入するには、2つの行の間に行を挿入し、その行の種類を [**リレーションシップ**] に変更します。 [ **relmoveto** ] 行が2つの行の間にある場合は、図形のパスにある改行の後の行の最初の頂点に対する*x*座標と*y*座標を格納します。 
  

