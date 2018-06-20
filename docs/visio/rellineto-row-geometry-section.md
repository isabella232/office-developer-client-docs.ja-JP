---
title: '[RelLineTo] 行 ([図形座標] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: 含まれています - x と y の図形の幅と高さを基準にして、直線の線分の終点の座標です。
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806187"
---
# <a name="rellineto-row-geometry-section"></a>[RelLineTo] 行 ([図形座標] セクション)

*X*が含まれています- と*y*の図形の幅と高さを基準にして、直線の線分の終点の座標です。 
  
> [!NOTE]
> **RelLineTo**行は、.vsdx、.vsdm、.vstx、.vstm、.vssx、および .vssm のファイル形式でのみ保持できます。 ファイル保存すると、Visio 2003 から 2010 年の書式には、 **RelLineTo**行が[[lineto]](lineto-row-geometry-section.md)行に変換されます。 
  
**RelLineTo**行には、次のセルが含まれています。 
  
|**Cell**|**説明**|
|:-----|:-----|
|[X](x-cell-geometry-section.md) <br/> |*X* -図形の幅を基準にして、直線の線分の終点の座標です。  <br/> |
|[Y](y-cell-geometry-section.md) <br/> |*Y* -図形の高さを基準にして、直線の線分の終点の座標です。  <br/> |
   
## <a name="remarks"></a>備考

**RelLineTo**行の値は、 [[lineto]](lineto-row-geometry-section.md)行で、幅と図形の高さを乗じた値に相当します。 例: **[lineto]** 行の [ **X** ] セルの値と数式があると**RelLineTo**の行の [ **X** ] セルの値が「0」、[ **Y** ] セルの値は「0.5」を置き換えることができます」*0"の幅] と [ **Y**セルは、数式"高さ*0.5」。 
  

