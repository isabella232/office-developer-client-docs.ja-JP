---
title: POLYLINE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251576
localization_priority: Normal
ms.assetid: 10baeec9-6c9b-b4ba-3138-7d1156a9e056
description: ポリラインを返します。 PolyLineTo ジオメトリの行のセルには、この関数が使用されます。
ms.openlocfilehash: afe31b3963cca03d0273b8768f6cc5538d1850ee
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806012"
---
# <a name="polyline-function"></a>POLYLINE 関数

ポリラインを返します。 PolyLineTo ジオメトリの行のセルには、この関数が使用されます。 
  
## <a name="syntax"></a>構文

ポリライン (* * *xType* * *、* * *yType* * *、* * *x1* * *、* * *y1* * *.) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |_X_の入力データを解釈する方法を指定します。 _XType_が 0 で、 _x_の入力のかどうかのデータの幅に対する割合として解釈されます。 _XType_が 1、入力_x_のかどうか、データはローカル座標として解釈されます。  <br/> |
| _yType_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |_Y_の解釈方法を指定のデータを入力します。 _YType_が 0、 _y_の入力のかどうかのデータは高さに対する割合として解釈されます。 _YType_が 1、 _y_の入力のかどうか、データはローカル座標として解釈されます。  <br/> |
| _x1_ <br/> |必須  <br/> |**番号** <br/> | _X_を調整します。  <br/> |
| _y1_ <br/> |必須  <br/> |**番号** <br/> |_Y_の座標です。  <br/> |
   
## <a name="remarks"></a>注釈

すべての*x*引数では、必要があります、 *y*引数を指定します。それ以外の場合、エラーが返されます。 
  
## <a name="example"></a>例

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
幅 x 高さの寸法の四角形を返します。 
  

