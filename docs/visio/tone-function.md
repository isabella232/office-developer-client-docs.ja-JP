---
title: TONE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: int パラメーターで指定された量で鮮やかさを小さくして、色を変更します。
ms.openlocfilehash: c3352d4c15671244d0fc4701f2c26b4e0c2ea54d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335687"
---
# <a name="tone-function"></a>TONE 関数

_int_パラメーターで指定された量で鮮やかさを小さくして、色を変更します。 
  
## <a name="syntax"></a>構文

トーン (* * *color* * *、* * *int* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |Microsoft Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _int_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |色の鮮やかさを減少する量を指定します。 正または負の値を指定できます。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>解説

鮮やかさの上限と下限はそれぞれ 0 と 240 です。 _int_パラメーターに渡すことができる整数のサイズに制限はありませんが、鮮やかさがこれらの制限を超えることはありません。 
  

