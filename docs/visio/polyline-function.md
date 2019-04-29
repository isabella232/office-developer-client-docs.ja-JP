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
description: ポリラインを返します。 この関数は、[polylineto] geometry の行のセルで使用します。
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426297"
---
# <a name="polyline-function"></a>POLYLINE 関数

ポリラインを返します。 この関数は、[polylineto] geometry の行のセルで使用します。 
  
## <a name="syntax"></a>構文

ポリライン (* * *xType* * *、* * *yType* * *、* * *x1* * *、* * *y1* * *...) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |必須  <br/> |**Boolean** <br/> |_x_入力データを解釈する方法を指定します。 _xType_が0の場合、入力データ_x_は幅に対する割合として解釈されます。 _xType_が1の場合、入力_x_データはローカル座標として解釈されます。  <br/> |
| _yType_ <br/> |必須  <br/> |**Boolean** <br/> |_y_入力データの解釈方法を指定します。 _yType_が0の場合、入力の_y_データは、高さの割合として解釈されます。 _yType_が1の場合、入力の_y_データはローカル座標として解釈されます。  <br/> |
| _x1_ <br/> |必須  <br/> |**数値** <br/> | _x_座標を示します。  <br/> |
| _y1_ <br/> |必須  <br/> |**数値** <br/> |_y_座標を示します。  <br/> |
   
## <a name="remarks"></a>注釈

すべての*x*引数に対して、 *y*引数が必要です。それ以外の場合は、エラーが返されます。 
  
## <a name="example"></a>例

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
幅 x 高さの寸法の四角形を返します。 
  

