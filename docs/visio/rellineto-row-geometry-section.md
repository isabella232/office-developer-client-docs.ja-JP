---
title: '[RelLineTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: 図形の幅と高さを基準にした直線セグメントの終了頂点の x 座標と y 座標を含む。
ms.openlocfilehash: 24f9f5c7de5b71f451f4d2e907d56516cc3b3c25
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570177"
---
# <a name="rellineto-row-geometry-section"></a>[RelLineTo] 行 ([図形座標] セクション)

図形の  *幅*  と高さを基準にした直線セグメントの終了頂点の x 座標と  *y*  座標を含む。 
  
> [!NOTE]
> [**RelLineTo**] 行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保存できます。 ファイルを 2003- 2010 形式Visio保存すると **、RelLineTo** 行は [LineTo 行に変換](lineto-row-geometry-section.md)されます。 
  
[**RelLineTo**] 行には次のセルが含まれます。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |図形  *の*  幅を基準にした直線セグメントの終了頂点の x 座標。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |図形  *の高*  さを基準にした直線セグメントの終了頂点の y 座標。  <br/> |
   
## <a name="remarks"></a>注釈

[**RelLineTo**] 行の値は、図形の幅と高さを乗算した [[LineTo](lineto-row-geometry-section.md)] 行の値に等しくなります。 たとえば **、X** セルの値が "0" で **、Y** セルの値が "0.5" の **RelLineTo** 行は **、X** セルの値が数式 "Width *0" で **、Y*** セルが数式 "Height 0.5" である **LineTo** 行に置き換えます。 
  

