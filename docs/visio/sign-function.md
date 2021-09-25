---
title: SIGN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
ms.localizationpriority: medium
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: 数値の符号を表す値を返します。
ms.openlocfilehash: ea7ed2ec4cacb6d926d907934f8745b8ab7538ad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622823"
---
# <a name="sign-function"></a>SIGN 関数

数値の符号を表す値を返します。 
  
## <a name="syntax"></a>構文

SIGN(** *number* **, ** *fuzz* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> | 符号を確認する数値を指定します。  <br/> |
| _ファズ_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |指定した数値と 0 との誤差を指定します。数値と 0 の差がこの誤差以内である場合に、数値は 0 として扱われます。  <br/> |
   
### <a name="return-value"></a>戻り値

数値型 (Numeric)
  
## <a name="remarks"></a>注釈

SIGN 関数は、数値が正の場合は 1、数値が 0 の場合は 0、数値が負の場合は -1 _を返_ します。 
  
あいまいな値  _を指定すると_ 、計算がほぼ 0 の場合に浮動小数点の丸めエラーを回避できます。 ファジー値を指定しない場合、Visio 1E-9 (0.0000000001) を使用します。 図面の縮尺を変更したり、正確な比較を行う場合は、異なる値を指定できます。 
  
## <a name="example-1"></a>例 1

SIGN(-5)
  
-1 を返します。
  
## <a name="example-2"></a>例 2

SIGN(0)
  
0 を返します。
  
## <a name="example-3"></a>例 3

SIGN(0.000000000001)
  
0 を返します。
  
## <a name="example-4"></a>例 4

SIGN(0.000000000001,0)
  
1 を返します。
  

