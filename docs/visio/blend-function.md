---
title: BLEND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: Float 型パラメーターで指定された比率で 2 つの色をブレンドします。
ms.openlocfilehash: 61993cea9eed6583d62004e1c756368b67c7bb33
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804899"
---
# <a name="blend-function"></a>BLEND 関数

_Float 型_パラメーターで指定された比率で 2 つの色をブレンドします。 
  
## <a name="syntax"></a>構文

ブレンド (* * *color1* * *、* * *color2* * *、* * *[0, 1] の浮動小数点数** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |最初の色の Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _color2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |2 番目の色の Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _float [0, 1]_ <br/> |必須  <br/> |**Float** <br/> |_Color2_と_color1_をそれぞれブレンドする割合。 実数 0 ~ 1 にします。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>注釈

返される色は、 _color2_と_color1_のそれぞれに、_浮動小数点_パラメーターで指定されているブレンドするための相対的比率によって決定されます。 _Float_が 0.25 の場合は、返されるカラーは構成の 75% の_color1_と_color2_の 25% です。 
  
考える別の方法では、 _color2_に_color1_のカラー スペクトルに沿ってポイントを_float 型_の値が対応します。 したがって、小さい番号 (0 に近い)_浮動小数点数_の生成ブレンド近くするには_color1_、大きい数値 (1 に近い) 中に生成_color2_に近い場所にブレンド用です。
  

