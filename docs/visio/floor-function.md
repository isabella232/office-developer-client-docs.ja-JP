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
description: または複数の次のインスタンスを次の整数には、数値を 0 (ゼロ) を四捨五入します。
ms.openlocfilehash: f66b993e3ab48fd1abc685b7db5889d5bf24fbfc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805397"
---
# <a name="floor-function"></a>FLOOR 関数

次の整数、または_複数_の次のインスタンスには、数値を 0 (ゼロ) を丸めます。
  
## <a name="syntax"></a>構文

フロア (* **番号** *、* **複数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _number_ <br/> |必須  <br/> |**番号** <br/> |切り上げの対象となる数値を指定します。  <br/> |
| _複数_ <br/> |必須  <br/> |**番号** <br/> |切り上げの対象となる倍数値を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

数値
  
## <a name="remarks"></a>備考

_複数_を指定しない場合、数は、次の整数を 0 方向に丸めます。 
  
 _番号_と_複数_は、同一の記号、または、#NUM を持つ必要があります! エラーが返されます。 #Value! の値には、_番号_または_複数_のいずれかを変換できません! 場合、 エラーが返されます。 _番号_または_複数_のいずれかが 0 の場合、結果は 0 になります。 
  
## <a name="example-1"></a>例 1

FLOOR(3.7)
  
3 を返します。
  
## <a name="example-2"></a>例 2

FLOOR(-3.7)
  
-3 を返します。
  
## <a name="example-3"></a>例 3

フロア (3.7, 0.5)
  
3.5 を返します。
  

