---
title: TRUNC 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
localization_priority: Normal
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: 指定した桁数に切り詰められた数値を返します。
ms.openlocfilehash: 5b2138ff3091f70313344d5b38d8225d572d8e70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426500"
---
# <a name="trunc-function"></a>TRUNC 関数

指定した桁数に切り詰められた数値を返します。
  
## <a name="syntax"></a>構文

TRUNC (* * *number* * *, * * *numberofdigits* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |切り捨ての対象となる数値を指定します。  <br/> |
| _numberofdigits_ <br/> |必須  <br/> |**数値** <br/> |_数値_を切り捨てる桁数を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値型
  
## <a name="remarks"></a>注釈

_numberofdigits_が0より大きい場合、引数_number_は、その小数点の右側にある_numberofdigits_に切り捨てられます。 _numberofdigits_が0の場合、_数値_は整数に切り捨てられます。 _numberofdigits_が0より小さい場合、_数値_は、その小数点の左側の_numberofdigits_に切り捨てられます。 
  
## <a name="example-1"></a>例 1

TRUNC (123.654, 2)
  
123.65 を返します。
  
## <a name="example-2"></a>例 2

TRUNC (123.654, 0)
  
123 を返します。
  
## <a name="example-3"></a>例 3

TRUNC (123.654,-1)
  
120 を返します。
  

