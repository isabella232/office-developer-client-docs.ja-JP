---
title: TINT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c4f176d6-4af0-282d-5640-7d98e84dfb55
description: int パラメーターで指定された量 (正または負) で明るさを増やして色を変更します。
ms.openlocfilehash: 2dbc354ee08ddfab1e9d1f24bad9612e4f20839b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627297"
---
# <a name="tint-function"></a>TINT 関数

int パラメーターで指定された量 (正または負) で明るさを増やして色  _を変更_ します。 
  
## <a name="syntax"></a>構文

TINT(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |Microsoft Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _int_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |色の輝度を増加する量を指定します。正または負の値を指定できます。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>注釈

明度の上限と下限は、それぞれ 0 と 240 です。 _int_ パラメーターに渡す整数のサイズに制限はありません。ただし、明度がこれらの制限を超える場合はありません。 
  

