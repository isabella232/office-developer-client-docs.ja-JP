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
description: X を返しますが、ローカル座標系で) の 2 本の線が交差する点の座標です。
ms.openlocfilehash: ea5a08f25f3e45dab3fe3fd83b74cf9a7541b6e6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805588"
---
# <a name="intersectx-function"></a>INTERSECTX 関数

*X*を返しますが、ローカル座標系で) の 2 本の線が交差する点の座標です。 
  
## <a name="syntax"></a>構文

INTERSECTX (* * *x1* * *、* * *y1* * *、* * *angle1* * *、* * *x2* * *、* * *y2* * *、* * *angle2* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _x1_ <br/> |必須  <br/> |**番号** <br/> |_X_の最初の行の上の点の座標です。  <br/> |
| _y1_ <br/> |必須  <br/> |**番号** <br/> |_Y_-最初の行の上の点の座標です。  <br/> |
| _angle1_ <br/> |必須  <br/> |**番号** <br/> | 1 本目の線の [Angle] セルにある値を指定します。  <br/> |
| _x2_ <br/> |必須  <br/> |**番号** <br/> |_X_の 2 番目の線上の点の座標です。  <br/> |
| _y2_ <br/> |必須  <br/> |**番号** <br/> |_Y_の 2 つ目のライン上の点の座標です。  <br/> |
| _angle2_ <br/> |必須  <br/> |**番号** <br/> |2 本目の線の [Angle] セルにある値を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

数値
  
## <a name="remarks"></a>備考

各明細行は、点 (*x, y*) と角度として定義されます。 
  
Microsoft Visio で、この関数は、回転したガイドに接着されている図形の [PinX] セルで使用されます。 
  
2 本の線が交差しない場合、この関数はゼロで除算したことを示すエラー (#DIV/0!) を返します。Visio ではこのエラーは無視され、最後に設定された点の座標値を復元します。 
  
## <a name="example"></a>例

INTERSECTX (VertGuide!VertGuide [pinx]![Piny]、VertGuide!HorzGuide の角度です。HorzGuide [pinx]![Piny]、HorzGuide!角度) 
  
*X*を返します-ページ単位での交差ポイントの VertGuide と HorzGuide の座標です。 
  

