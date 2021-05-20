---
title: FLOOR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251423
localization_priority: Normal
ms.assetid: 6788bc96-cc86-5f21-781f-67274e7f605a
description: 数値を 0 (ゼロ)、次の整数、または倍数の次のインスタンスに丸します。
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439899"
---
# <a name="floor-function"></a>FLOOR 関数

数値を 0 (ゼロ)、次の整数、または複数の次のインスタンスに丸  _められます_。
  
## <a name="syntax"></a>構文

FLOOR(** *number* **, ** *multiple* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |切り上げの対象となる数値を指定します。  <br/> |
| _複数_ <br/> |必須  <br/> |**数値** <br/> |切り上げの対象となる倍数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

番号
  
## <a name="remarks"></a>注釈

multiple  _を_ 指定しない場合、数値は 0 から次の整数に向かって丸められます。 
  
 _数値_ と  _倍数は_ 、同じ記号、または複数の記号#NUM! エラーを返します。 数値または  _複数_ の  _値_ に変換できない場合は、値#VALUE! エラーを返します。 数値または _倍数__が_ 0 の場合、結果は 0 になります。 
  
## <a name="example-1"></a>例 1

FLOOR(3.7)
  
3 を返します。
  
## <a name="example-2"></a>例 2

FLOOR(-3.7)
  
-3 を返します。
  
## <a name="example-3"></a>例 3

FLOOR(3.7, 0.5)
  
3.5 を返します。
  

