---
title: SIGN 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251497
localization_priority: Normal
ms.assetid: fdc032c2-d0bd-1592-de3f-33c478d066ee
description: 数値の符号を表す値を返します。
ms.openlocfilehash: 34bbbab17de94b0a8c95b4b0bfd3829a06dc7e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420655"
---
# <a name="sign-function"></a>SIGN 関数

数値の符号を表す値を返します。 
  
## <a name="syntax"></a>構文

SIGN (* * *number* * *, * **ファジー* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> | 符号を確認する数値を指定します。  <br/> |
| _ファジー_ <br/> |省略可能  <br/> |**数値** <br/> |指定した数値と 0 との誤差を指定します。数値と 0 の差がこの誤差以内である場合に、数値は 0 として扱われます。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

SIGN 関数は、 _number_が正の場合は1、 __ 数値が0の場合は0、_数値_が負の場合は-1 を返します。 
  
_ファジー_値を指定すると、計算がほぼゼロの場合に浮動小数点 roundoff エラーを回避できます。 _ファジー_値を指定しない場合、Visio は 1e-9 (0.000000001) を使用します。 図面の縮尺を変更したり、正確な比較を行う場合は、異なる値を指定できます。 
  
## <a name="example-1"></a>例 1

符号 (-5)
  
-1 を返します。
  
## <a name="example-2"></a>例 2

符号 (0)
  
0 を返します。
  
## <a name="example-3"></a>例 3

記号 (0.00000000001)
  
0 を返します。
  
## <a name="example-4"></a>例 4

符号 (0.00000000001, 0)
  
1 を返します。
  

