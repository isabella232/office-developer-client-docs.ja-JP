---
title: INTERSECTX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
ms.localizationpriority: medium
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: 2 つの線が交差する点の x 座標 (ローカル座標系) を返します。
ms.openlocfilehash: 0b8c22357c6eb6ac6b5d0fc43117f0749dd1b106
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554559"
---
# <a name="intersectx-function"></a>INTERSECTX 関数

2 つの  *線が*  交差する点の x 座標 (ローカル座標系) を返します。 
  
## <a name="syntax"></a>構文

INTERSECTX(** *x1* **, ** *y1* **, ** *angle1* **, ** *x2* **, ** *y2* **, ** *angle2* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |必須  <br/> |**数値** <br/> |1  _行_ 目の点の x 座標。  <br/> |
| _y1_ <br/> |必須  <br/> |**数値** <br/> |1 行目の点の  _y_ 座標。  <br/> |
| _angle1_ <br/> |必須かどうか  <br/> |**数値** <br/> | 1 本目の線の [Angle] セルにある値を指定します。  <br/> |
| _x2_ <br/> |必須  <br/> |**数値** <br/> |2  _行_ 目の点の x 座標。  <br/> |
| _y2_ <br/> |必須  <br/> |**数値** <br/> |2 行目の点の  _y_ 座標。  <br/> |
| _angle2_ <br/> |必須かどうか  <br/> |**数値** <br/> |2 本目の線の [Angle] セルにある値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

各線は点 (*x,y*) と角度によって定義されます。 
  
Microsoft Visio で、この関数は、回転したガイドに接着されている図形の [PinX] セルで使用されます。 
  
2 本の線が交差しない場合、この関数はゼロで除算したことを示すエラー (#DIV/0!) を返します。Visio ではこのエラーは無視され、最後に設定された点の座標値を復元します。 
  
## <a name="example"></a>例

INTERSECTX(VertGuide!PinX,VertGuide!PinY,VertGuide!Angle, HorzGuide!PinX,HorzGuide!PinY,HorzGuide!角度) 
  
ページ単位でVertGuide と HorzGuide の交点の x 座標を返します。 
  

