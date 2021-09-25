---
title: POW 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251483
ms.localizationpriority: medium
ms.assetid: c6519c55-5f98-ed0d-95b1-5443d0d23c0b
description: 指数の出力に上げられた数値を返します。
ms.openlocfilehash: 5c829bb4ec236b251cc258fed6d2c862ede54980
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570331"
---
# <a name="pow-function"></a>POW 関数

指数の出力に上げられた数値を返します。
  
## <a name="syntax"></a>構文

POW(** *number* **, ** *exponent* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須かどうか  <br/> |**数値** <br/> |指数で累乗する数値を指定します。  <br/> |
| _exponent_ <br/> |必須かどうか  <br/> |**数値** <br/> |指数を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

数値 _と__指数の両方が_ 整数以外で、負の値を指定できます。 _数値が_ 0 ではなく、_指数_ が 0 の場合、この関数は 1 を返します。 _数値が_ 0 で、_指数が_ 負の場合、この関数は 0.0 を返します。 数値と _指数_ の _両方_ が 0 の場合、または _数値_ が負で指数が整数ではない場合、この関数は 0.0 を返します。 数値と _指数の__両方が負_ の場合、この関数は -1.#IND を返します。 
  
## <a name="example"></a>例

POW(5,2) 
  
25 を返します。 
  

