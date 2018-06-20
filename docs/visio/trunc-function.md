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
description: 指定された桁数に切り捨てられる数を返します。
ms.openlocfilehash: 8f6a9798391d308a234469d93bc8f481de5fc8da
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806688"
---
# <a name="trunc-function"></a>TRUNC 関数

指定された桁数に切り捨てられる数を返します。
  
## <a name="syntax"></a>構文

TRUNC (* **番号** *、* * *numberofdigits* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |切り捨ての対象となる数値を指定します。  <br/> |
| _numberofdigits_ <br/> |必須  <br/> |**数値** <br/> |切り捨てる_数値_を桁の数です。  <br/> |
   
### <a name="return-value"></a>�߂�l

数値
  
## <a name="remarks"></a>注釈

_Numberofdigits_が 0 より大きい場合は、_数値_は小数点の右側に_numberofdigits_に切り捨てられます。 _Numberofdigits_が 0 の場合は、_数値_が整数に切り捨てられます。 _Numberofdigits_が 0 より小さい場合は、_数値_は小数点の左側に_numberofdigits_に切り捨てられます。 
  
## <a name="example-1"></a>例 1

TRUNC(123.654,2)
  
123.65 を返します。
  
## <a name="example-2"></a>例 2

TRUNC(123.654,0)
  
123 を返します。
  
## <a name="example-3"></a>例 3

TRUNC(123.654,-1)
  
120 を返します。
  

