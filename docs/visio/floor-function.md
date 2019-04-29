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
description: 数値を 0 (ゼロ) の方向、次の整数、または複数の次のインスタンスに切り上げます。
ms.openlocfilehash: 7a16a77a990180f34dd7a5706c24ec3232438467
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439899"
---
# <a name="floor-function"></a>FLOOR 関数

数値を 0 (ゼロ) の方向、次の整数、または_複数_の次のインスタンスに切り上げます。
  
## <a name="syntax"></a>構文

床面 (* **数値** *, * * *multiple* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |切り上げの対象となる数値を指定します。  <br/> |
| _マルチ_ <br/> |必須  <br/> |**数値** <br/> |切り上げの対象となる倍数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>注釈

_multiple_が指定されていない場合、数値は0に近づくと次の整数に丸められます。 
  
 _数値_と_複数_の値は、同じ記号または #NUM である必要があります。 エラーを返します。 _数値_、または_複数_の値を値に変換できない場合は、#VALUE します。 エラーを返します。 _数値_または_倍数_が0の場合、結果は0になります。 
  
## <a name="example-1"></a>例 1

床 (3.7)
  
3 を返します。
  
## <a name="example-2"></a>例 2

床面 (-3.7)
  
-3 を返します。
  
## <a name="example-3"></a>例 3

床面 (3.7, 0.5)
  
3.5 を返します。
  

