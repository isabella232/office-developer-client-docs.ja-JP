---
title: NURBS 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
ms.localizationpriority: medium
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: 非一次有理 B スプライン (NURBS) を返します。 この関数は、NURBSTo ジオメトリ行の E セルで使用されます。
ms.openlocfilehash: 335b055aef4517a783a7971e9f63bc36fea9dc4c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590185"
---
# <a name="nurbs-function"></a>NURBS 関数

非一次有理 B スプライン (NURBS) を返します。 この関数は、NURBSTo ジオメトリ行の E セルで使用されます。
  
## <a name="syntax"></a>構文

NURBS(** *knotLast* **, ** *degree* **, ** xType **, ** *yType* **, ** x1 **,  ** *y1* **, ** knot1 **, **  *weight1* **, ..)  
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _knotLast_ <br/> |必須かどうか  <br/> |**string** <br/> | 最後のノットを指定します。  <br/> |
| _度_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |スプラインの角度を指定します。  <br/> |
| _xType_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |x 入力データの解釈方法  _を_ 指定します。 _xType が_ 0 の場合、_すべての x_ 入力データは Width のパーセンテージとして解釈されます。 _xType が_ 1 の場合、_すべての x_ 入力データはローカル座標として解釈されます。  <br/> |
| _yType_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |y 入力データの  _解釈方法を_ 指定します。 _yType が_ 0 の場合、_すべての y_ 入力データは Height のパーセンテージとして解釈されます。 _yType が_ 1 の場合、_すべての y_ 入力データはローカル座標として解釈されます。  <br/> |
| _x1_ <br/> |必須  <br/> |**String** <br/> |x 座標を指定します。  <br/> |
| _y1_ <br/> |必須  <br/> |**String** <br/> |y 座標を指定します。  <br/> |
| _knot1_ <br/> |必須  <br/> |**String** <br/> |B スプライン上のノットを指定します。  <br/> |
| _weight1_ <br/> |必須  <br/> |**String** <br/> |B スプラインの太さを指定します。  <br/> |
   
## <a name="remarks"></a>注釈

x 引数  *ごとに y*  引数  *が必要*  です。それ以外の場合は、エラーが返されます。 
  
少なくとも 1 つの *x、y*、ノット、*および weight* 引数を *指定する必要* があります。それ以外の場合Visioエラーが返されます。 
  

