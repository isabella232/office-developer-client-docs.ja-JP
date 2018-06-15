---
title: GRAVITY 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251433
localization_priority: Normal
ms.assetid: db80f147-71a0-0b23-bc7e-fe1915dfdd21
description: テキスト ブロックの正確なテキストの上下が逆にならないようにするのには指定された図形の回転の回転角度を計算します。
ms.openlocfilehash: 0d8b0160c7e7d63fb5a272219a2694d35e6e6b61
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805487"
---
# <a name="gravity-function"></a>GRAVITY 関数

テキスト ブロックの正確なテキストの上下が逆にならないようにするのには指定された図形の回転の回転角度を計算します。
  
## <a name="syntax"></a>構文

重力加速度 (* **角度** *、[* * *limit1* * *]、[* * *limit2* * *]) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _角度_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 図形の角度を指定します。  <br/> |
| _limit1_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |回転の最初の制限角度を指定します。既定の制限角度は 90°です。  <br/> |
| _limit2_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |回転の 2 番目の制限角度を指定します。既定の制限角度は 270°です。  <br/> |
   
### <a name="return-value"></a>�߂�l

文字列
  
## <a name="remarks"></a>注釈

通常、GRAVITY 関数は [TxtAngle] セルで使用します。 
  
_Limit1_および_limit2_; で指定された値の間_の角度_の場合、返される値は 180 度それ以外の場合戻り値は、0 度です。
  
すべての引数は、関数によって自動的に 0 ～ 360°の範囲に正規化されます。引数に単位を指定しないと、ラジアンが使用されます。 
  
## <a name="example-1"></a>例 1

GRAVITY(Angle)
  
180 度の*角度*が 90、270 度の間にある場合を返します。それ以外の場合、0 度を返します。 
  
## <a name="example-2"></a>例 2

GRAVITY(2)
  
2 ラジアンは 90 ～ 270°の範囲に含まれるため、180°を返します。
  
## <a name="example-3"></a>例 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
0°を返します。
  
## <a name="example-4"></a>例 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
0°を返します。
  

