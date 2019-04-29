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
description: 指定した図形の回転のテキストブロックの正確な角度を計算し、テキストが逆さまになるのを防ぎます。
ms.openlocfilehash: 77c944d954292e231f8bacbe3c8a4433aad5d689
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429286"
---
# <a name="gravity-function"></a>GRAVITY 関数

指定した図形の回転のテキストブロックの正確な角度を計算し、テキストが逆さまになるのを防ぎます。
  
## <a name="syntax"></a>構文

重力 (* **角度** *、[* **制限 1* * *]、[* * *limit2* * *]) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _直交_ <br/> |必須  <br/> |**String** <br/> | 図形の角度を指定します。  <br/> |
| _制限1_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |回転の最初の制限角度を指定します。 既定の制限角度は 90°です。  <br/> |
| _limit2_ <br/> |省略可能  <br/> |**文字列型 (String)** <br/> |回転の 2 番目の制限角度を指定します。 既定の制限角度は 270°です。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

通常、GRAVITY 関数は [TxtAngle] セルで使用します。 
  
_角度_が_制限 1_および_limit2_で指定された値の間にある場合、返される値は180°になります。それ以外の場合、返される値は0°です。
  
すべての引数は、関数によって自動的に 0 ～ 360°の範囲に正規化されます。 引数に単位を指定しないと、ラジアンが使用されます。 
  
## <a name="example-1"></a>例 1

重力 (角度)
  
*角度*が 90 ~ 270 度の場合、180°を返します。それ以外の場合は0°を返します。 
  
## <a name="example-2"></a>例 2

重力 (2)
  
2 ラジアンは 90 ～ 270°の範囲に含まれるため、180°を返します。
  
## <a name="example-3"></a>例 3

GRAVITY(100 deg, 110 deg, 290 deg)
  
0°を返します。
  
## <a name="example-4"></a>例 4

GRAVITY(100 deg, 290 deg, 110 deg)
  
0°を返します。
  

