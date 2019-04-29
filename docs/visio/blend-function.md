---
title: BLEND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: float パラメーターで指定された比率で2つの色を合成します。
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432787"
---
# <a name="blend-function"></a>BLEND 関数

_float_パラメーターで指定された比率で2つの色を合成します。 
  
## <a name="syntax"></a>構文

BLEND (* * *color1* * *、* * *color2* * *、* * *float [0, 1]* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |必須  <br/> |**数値** <br/> |最初の色の Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _color2_ <br/> |必須  <br/> |**数値** <br/> |2 番目の色の Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _float [0, 1]_ <br/> |必須  <br/> |**Float** <br/> |_color2_と_color1_をそれぞれブレンドする比率を指定します。 0 ～ 1 の実数を使用します。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>注釈

返される色は、 _float_パラメーターで指定されたように、 _color2_と_color1_をそれぞれブレンディングする相対的な比率によって決まります。 たとえば、 _float_が0.25 の場合、返される色は_color1_の 75%、 _color2_の 25% で構成されます。 
  
この点を考慮するもう1つの方法は、_浮動小数点_値が、 _color1_から_color2_へのカラースペクトルに沿った点に対応していることです。 そのため、_浮動小数点型_( _color1_) の値が小さいほど、より大きな数値 (1 に近い) は、 _color2_に近い値になります。
  

