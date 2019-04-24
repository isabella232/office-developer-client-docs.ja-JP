---
title: ROUND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
localization_priority: Normal
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: numberofdigits で表される精度に数値を丸めます。
ms.openlocfilehash: 6795cbc4d99e293da06c0ec369d2cefb84f9f5b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315576"
---
# <a name="round-function-visioshapesheet"></a>ROUND 関数 (VisioShapeSheet)

*numberofdigits*で表される精度に数値を丸めます。 
  
## <a name="syntax"></a>構文

ROUND (* **数値** *、* * *numberofdigits* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |四捨五入の対象となる数値を指定します。  <br/> |
| _numberofdigits_ <br/> |必須  <br/> |**数値** <br/> |精度の小数点以下桁数を指定します。  <br/> |
   
## <a name="remarks"></a>解説

_numberofdigits_が0より大きい場合、_数値_は、 _numberofdigits_の小数点の右側に切り上げられます。 _numberofdigits_が0の場合、_数値_は整数に丸められます。 _numberofdigits_が0より小さい場合、_数値_は、 _numberofdigits_の小数点の左に丸められます。 
  
## <a name="example-1"></a>例 1

ROUND (123.654、2)
  
123.65 を返します。
  
## <a name="example-2"></a>例 2

ROUND (123.654, 0)
  
124 を返します。
  
## <a name="example-3"></a>例 3

ROUND (123.654,-1)
  
120 を返します。
  

