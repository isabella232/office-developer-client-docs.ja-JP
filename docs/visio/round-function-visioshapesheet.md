---
title: ROUND 関数 (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251491
ms.localizationpriority: medium
ms.assetid: a374fe7d-7302-5365-81ab-64f5474d9d5c
description: 数値を numberofdigits で表される精度に丸します。
ms.openlocfilehash: e004542ba0cd8b804893698045d3f9d67737b520
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554076"
---
# <a name="round-function-visioshapesheet"></a>ROUND 関数 (VisioShapeSheet)

数値を  *numberofdigits*  で表される精度に丸します。 
  
## <a name="syntax"></a>構文

ROUND(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須かどうか  <br/> |**数値** <br/> |四捨五入の対象となる数値を指定します。  <br/> |
| _numberofdigits_ <br/> |必須かどうか  <br/> |**数値** <br/> |精度の小数点以下桁数を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

_numberofdigits が_ 0 より大きい場合、数値は小数点の右側の _numberofdigits_ で四捨五入されます。 _numberofdigits が_ 0 の場合、_数値は_ 整数に丸められます。 _numberofdigits が_ 0 より小さい場合、数値は小数点の左側に _numberofdigits_ で四捨五入されます。 
  
## <a name="example-1"></a>例 1

ROUND(123.654,2)
  
123.65 を返します。
  
## <a name="example-2"></a>例 2

ROUND(123.654,0)
  
124 を返します。
  
## <a name="example-3"></a>例 3

ROUND(123.654,-1)
  
120 を返します。
  

