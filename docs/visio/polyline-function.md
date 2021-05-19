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
description: ポリラインを返します。 この関数は、PolyLineTo ジオメトリ行の [A] セルで使用されます。
ms.openlocfilehash: d801c6f2c1a81cc5cc99b3517c4d86784421d7e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426297"
---
# <a name="polyline-function"></a>POLYLINE 関数

ポリラインを返します。 この関数は、PolyLineTo ジオメトリ行の [A] セルで使用されます。 
  
## <a name="syntax"></a>構文

POLYLINE(** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **..) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _xType_ <br/> |必須  <br/> |**Boolean** <br/> |x 入力データの解釈方法  _を_ 指定します。 _xType が_ 0 の場合、入力 _x_-data は Width のパーセンテージとして解釈されます。 _xType が_ 1 の場合、入力 _x_-data はローカル座標として解釈されます。  <br/> |
| _yType_ <br/> |必須  <br/> |**Boolean** <br/> |y -input データの  _解釈方法_ を指定します。 _yType が_ 0 の場合、入力 _y_-data は Height のパーセンテージとして解釈されます。 _yType が_ 1 の場合、入力 _y_-data はローカル座標として解釈されます。  <br/> |
| _x1_ <br/> |必須  <br/> |**数値** <br/> | _x_ 座標。  <br/> |
| _y1_ <br/> |必須  <br/> |**数値** <br/> |_y_ 座標。  <br/> |
   
## <a name="remarks"></a>注釈

x 引数  *ごとに y*  引数  *が必要*  です。それ以外の場合は、エラーが返されます。 
  
## <a name="example"></a>例

POLYLINE (0, 0, 0, 0, 0, 1, 1, 1, 1, 0, 0, 0) 
  
幅 x 高さの寸法の四角形を返します。 
  

