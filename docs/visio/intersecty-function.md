---
title: INTERSECTY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251445
localization_priority: Normal
ms.assetid: a298eead-044b-6f40-54c7-e0e6088baa19
description: 2本の線が交わる点の y 座標 (ローカル座標系) を返します。
ms.openlocfilehash: 6fcd06e7086d52b9c45f1deb9d4c191f1a7b1fd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335260"
---
# <a name="intersecty-function"></a>INTERSECTY 関数

2本の線が交わる点の*y*座標 (ローカル座標系) を返します。 
  
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

番号
  
## <a name="remarks"></a>解説

各線は点 (*x,y*) と角度によって定義されます。 
  
Microsoft Visio で、この関数は、回転したガイドに接着されている図形の [PinY] セルで使用されます。 
  
2 本の線が交差しない場合、この関数はゼロで除算したことを示すエラー (#DIV/0!) を返します。Visio ではこのエラーは無視され、最後に設定された点の座標値を復元します。 
  
## <a name="example"></a>例

INTERSECTY (vertguide!PinX、vertguide!PinY、vertguide!Angle、HorzGuide!PinX、HorzGuide!PinY、HorzGuide!直交 
  
vertguide と HorzGuide の交差点の*y*座標をページ単位で返します。 
  

