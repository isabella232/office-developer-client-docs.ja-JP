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
description: 次の複数のインスタンスには、0 (ゼロ) から数値を丸めます。 複数を指定しない場合、次の整数を 0 から数に丸めます。
ms.openlocfilehash: fa982b44ea4a73e7da614c49a52cd50efd612f20
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804955"
---
# <a name="ceiling-function"></a>CEILING 関数

_複数_の次のインスタンスを 0 (ゼロ) から数値を四捨五入します。 _複数_を指定しない場合、次の整数に 0 から番号を丸めます。 
  
## <a name="syntax"></a>構文

天井 (* **番号** *、* **複数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**番号** <br/> |切り上げの対象となる数値を指定します。  <br/> |
| _複数_ <br/> |必須  <br/> |**番号** <br/> |丸めを行う複数。  <br/> |
   
## <a name="remarks"></a>注釈

 _番号_と_複数_は、同一の記号、または、#NUM を持つ必要があります! エラーが返されます。 #Value! の値には、_番号_または_複数_のいずれかを変換できません! 場合、 エラーが返されます。 _番号_または_複数_のいずれかが 0 の場合、結果は 0 になります。 
  
## <a name="example-1"></a>例 1

CEILING(3.7)
  
4 を返します
  
## <a name="example-2"></a>例 2

CEILING(-3.7)
  
-4 を返します
  
## <a name="example-3"></a>例 3

天井 (3.7, 0.25)
  
3.75 を返します
  

