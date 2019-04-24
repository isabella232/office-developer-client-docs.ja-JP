---
title: TINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: int パラメーターで指定された正または負の値で明度を増やして色を変更します。
ms.openlocfilehash: 8924bc0662814e14d01b4bd5332f5fadeb0a1082
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32280932"
---
# <a name="tint-function"></a>TINT 関数

_int_パラメーターで指定された正または負の値で明度を増やして色を変更します。 
  
## <a name="syntax"></a>構文

濃淡 (* * *color* * *、* * *int* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |Microsoft Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _int_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |色の輝度を増加する量を指定します。 正または負の値を指定できます。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>解説

明度の上限と下限は、それぞれ 0 と 240 です。 _int_パラメーターに渡すことができる整数のサイズに制限はありませんが、明度がこれらの制限を超えることはありません。 
  

