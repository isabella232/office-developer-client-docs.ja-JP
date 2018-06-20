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
ms.openlocfilehash: 5f812dc4313e15df5d66a919707e7cdbb79f94b9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806501"
---
# <a name="sign-function"></a>SIGN 関数

数値の符号を表す値を返します。 
  
## <a name="syntax"></a>構文

記号 (* **番号** *、* **ファジー* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> | 符号を確認する数値を指定します。  <br/> |
| _ファジー_ <br/> |省略可能  <br/> |**数値** <br/> |指定した数値と 0 との誤差を指定します。数値と 0 の差がこの誤差以内である場合に、数値は 0 として扱われます。  <br/> |
   
### <a name="return-value"></a>�߂�l

数値型 (Numeric)
  
## <a name="remarks"></a>注釈

SIGN 関数は、_数値_が正の場合に 1 を返します、負の_数_は、0 または-1 が_数値_の場合は 0 です。 
  
Specifyin_誤差_の値は、計算がほぼゼロの場合、浮動小数点の丸めエラーを避けるために役立ちます。 _ファジー_値を指定しない場合は、1e-9 (0.000000001) が使用されます。 または図面を拡大すると、厳密な比較をするときに異なる値を指定することがあります。 
  
## <a name="example-1"></a>例 1

SIGN(-5)
  
-1 を返します。
  
## <a name="example-2"></a>例 2

SIGN(0)
  
0 を返します。
  
## <a name="example-3"></a>例 3

SIGN(0.00000000001)
  
0 を返します。
  
## <a name="example-4"></a>例 4

SIGN(0.00000000001,0)
  
1 を返します。
  

