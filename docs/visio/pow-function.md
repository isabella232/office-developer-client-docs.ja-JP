---
title: POW 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
localization_priority: Normal
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: 指数で累乗した数値を返します。
ms.openlocfilehash: 7a1102aa13f54d7e323247b83af3732ebb63acf4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406312"
---
# <a name="pow-function"></a>POW 関数

指数で累乗した数値を返します。
  
## <a name="syntax"></a>構文

POW (* **数値** *、* **指数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |指数で累乗する数値を指定します。  <br/> |
| _exponent_ <br/> |必須  <br/> |**数値** <br/> |指数を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

数値と_指数_の両方とも整数ではない場合があり、負の_値_にすることもできます。 _数値_が0以外で、_指数_が0の場合、この関数は1を返します。 数値が0で、_指数_が負の_数_である場合、この関数は0.0 を返します。 _数値_と_指数_の両方が0の場合、または_数値_が負で、_指数_が整数ではない場合、この関数は0.0 を返します。 数値と_指数_の両方が負の_数_である場合、この関数は-1. #IND を返します。 
  
## <a name="example"></a>例

POW (5、2) 
  
25 を返します。 
  

