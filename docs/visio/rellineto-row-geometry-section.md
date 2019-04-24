---
title: '[RelLineTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: 図形の幅と高さに相対する直線セグメントの最後の頂点に対する x 座標と y 座標を格納します。
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320070"
---
# <a name="rellineto-row-geometry-section"></a>[RelLineTo] 行 ([図形座標] セクション)

図形の幅と高さに相対する直線セグメントの最後の頂点に対する*x*座標と*y*座標を格納します。 
  
> [!NOTE]
> [**RelLineTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 ファイルを Visio 2003-2010 形式に保存すると、[ **rellineto** ] 行は[lineto](lineto-row-geometry-section.md)行に変換されます。 
  
[**RelLineTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形の幅を基準にして、直線セグメントの最後の頂点に対する*x*座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形の高さを基準にして、直線セグメントの最後の頂点に対する*y*座標です。  <br/> |
   
## <a name="remarks"></a>解説

[**RelLineTo**] 行の値は、図形の幅と高さを乗算した [[LineTo](lineto-row-geometry-section.md)] 行の値に等しくなります。 例: [ **x** ] セルの値が "0" で、[ **y** ] セルの値が "0.5" である [ **lineto** ] 行に置き換えることができるのは、[ **x** ] セルの値が数式 "Width **** *0"、[ **y** ] セルが、数式 "Height*0.5." 
  

