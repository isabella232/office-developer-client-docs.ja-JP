---
title: INTERSECTX 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251444
localization_priority: Normal
ms.assetid: d8dc1915-f055-e858-1323-9e8c1cb7f2f1
description: 2本の線が交わる点の x 座標 (ローカル座標系) を返します。
ms.openlocfilehash: 857f81d667e33ad9ce79405ef5d59874903098e6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418275"
---
# <a name="intersectx-function"></a>INTERSECTX 関数

2本の線が交わる点の*x*座標 (ローカル座標系) を返します。 
  
## <a name="syntax"></a>構文

INTERSECTX (* * *x1* * *、* * *y1* * *、* * *angle1* * *、* * *x2* * *、* * *y2* * *、* * *angle2* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |必須  <br/> |**数値** <br/> |最初の線にある点の_x_座標です。  <br/> |
| _y1_ <br/> |必須  <br/> |**数値** <br/> |最初の線にある点の_y_座標です。  <br/> |
| _angle1_ <br/> |必須  <br/> |**数値** <br/> | 1 本目の線の [Angle] セルにある値を指定します。  <br/> |
| _x_ <br/> |必須  <br/> |**数値** <br/> |2番目の線にある点の_x_座標です。  <br/> |
| _y2_ <br/> |必須  <br/> |**数値** <br/> |2番目の線にある点の_y_座標です。  <br/> |
| _angle2_ <br/> |必須  <br/> |**数値** <br/> |2 本目の線の [Angle] セルにある値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

各線は点 (*x,y*) と角度によって定義されます。 
  
Microsoft Visio で、この関数は、回転したガイドに接着されている図形の [PinX] セルで使用されます。 
  
2 本の線が交差しない場合、この関数はゼロで除算したことを示すエラー (#DIV/0!) を返します。Visio ではこのエラーは無視され、最後に設定された点の座標値を復元します。 
  
## <a name="example"></a>例

INTERSECTX (vertguide!PinX、vertguide!PinY、vertguide!Angle、HorzGuide!PinX、HorzGuide!PinY、HorzGuide!直交 
  
vertguide と HorzGuide の交差点の*x*座標をページ単位で返します。 
  

