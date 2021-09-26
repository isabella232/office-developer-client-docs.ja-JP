---
title: TRUNC 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251508
ms.localizationpriority: medium
ms.assetid: 62f074ef-5bf8-df1e-d826-fc1027a36501
description: 指定した桁数に切り捨てられた数値を返します。
ms.openlocfilehash: d7a682fe413248af6da0eac6895f4e0a0a6de800
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603250"
---
# <a name="trunc-function"></a>TRUNC 関数

指定した桁数に切り捨てられた数値を返します。
  
## <a name="syntax"></a>構文

TRUNC(** *number* **, ** *numberofdigits* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |切り捨ての対象となる数値を指定します。  <br/> |
| _numberofdigits_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |数値を切り捨てる _桁数です。_  <br/> |
   
### <a name="return-value"></a>戻り値

数値型
  
## <a name="remarks"></a>注釈

_numberofdigits が_ 0 より大きい場合、数値は 10 進数の右側 _にある numberofdigits_ に切り捨てられて表示されます。 _numberofdigits が_ 0 の場合 _、数値_ は整数に切り詰められます。 _numberofdigits が_ 0 より小さい場合、数値は小数点の左側 _の numberofdigits_ に切り捨てられて表示されます。 
  
## <a name="example-1"></a>例 1

TRUNC(123.654,2)
  
123.65 を返します。
  
## <a name="example-2"></a>例 2

TRUNC(123.654,0)
  
123 を返します。
  
## <a name="example-3"></a>例 3

TRUNC(123.654,-1)
  
120 を返します。
  

