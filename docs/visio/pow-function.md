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
ms.openlocfilehash: 48870c679251a666a5756b2b684d262fe059eee0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806101"
---
# <a name="pow-function"></a>POW 関数

指数で累乗した数値を返します。
  
## <a name="syntax"></a>構文

POW (* **番号** *、* **指数** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**番号** <br/> |指数で累乗する数値を指定します。  <br/> |
| _exponent_ <br/> |必須  <br/> |**番号** <br/> |指数を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

_数値_と_指数_の両方に整数以外の場合、可能性があり、負の値になる場合があります。 _番号_が 0 と_指数_ではないかどうかは 0、1 を返します。 _数_が 0_の指数部_が負の場合、この関数は 0.0 を返します。 _数値_と_指数_の両方が 0 である場合、またはが負の_数_と_指数_が整数でない場合は、この関数は 0.0 を返します。 _数値_と_指数_の両方が負の値場合は、この関数は-1 を返します #IND.。 
  
## <a name="example"></a>例

POW(5,2) 
  
25 を返します。 
  

