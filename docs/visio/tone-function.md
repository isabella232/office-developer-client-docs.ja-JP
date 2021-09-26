---
title: TONE 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: c2d6a7dd-9f15-27bd-9623-2a047683ff98
description: int パラメーターで指定した量で彩度を下げ、色を変更します。
ms.openlocfilehash: 2ea8e6af43fe199e9c7bff18d1120b1e24d08eca
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627276"
---
# <a name="tone-function"></a>TONE 関数

int パラメーターで指定した量で彩度を下げ、色  _を変更_ します。 
  
## <a name="syntax"></a>構文

TONE(** *color* **, ** *int* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |Microsoft Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _int_ <br/> |必須  <br/> |**整数型 (Integer)** <br/> |色の鮮やかさを減少する量を指定します。正または負の値を指定できます。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>注釈

鮮やかさの上限と下限はそれぞれ 0 と 240 です。 _int_ パラメーターに渡す整数のサイズに制限はありません。ただし、彩度がこれらの制限を超える場合はありません。 
  

