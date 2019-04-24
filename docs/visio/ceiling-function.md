---
title: CEILING 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251405
localization_priority: Normal
ms.assetid: 1a8d6d48-7ae3-5483-28d2-5b1706088a53
description: 数値を 0 (ゼロ) から複数の次のインスタンスに切り上げます。 multiple が指定されていない場合、数値は0から次の整数に丸められます。
ms.openlocfilehash: 449f17d1b68c116cccb2635723a3f6277d0ac2a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337227"
---
# <a name="ceiling-function"></a>CEILING 関数

数値を 0 (ゼロ) から_複数_の次のインスタンスに切り上げます。 _multiple_が指定されていない場合、数値は0から次の整数に丸められます。 
  
## <a name="syntax"></a>構文

天井 (* **数値** *, * * *multiple* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**数値** <br/> |切り上げの対象となる数値を指定します。  <br/> |
| _マルチ_ <br/> |必須  <br/> |**数値** <br/> |複数のに丸める。  <br/> |
   
## <a name="remarks"></a>解説

 _数値_と_複数_の値は、同じ記号または #NUM である必要があります。 エラーを返します。 _数値_、または_複数_の値を値に変換できない場合は、#VALUE します。 エラーを返します。 _数値_または_倍数_が0の場合、結果は0になります。 
  
## <a name="example-1"></a>例 1

天井 (3.7)
  
4 を返します
  
## <a name="example-2"></a>例 2

天井 (-3.7)
  
-4 を返します
  
## <a name="example-3"></a>例 3

天井 (3.7、0.25)
  
3.75 を返します
  

