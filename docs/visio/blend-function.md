---
title: BLEND 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c67b46bb-0eb2-f094-2870-c320bd488705
description: float パラメーターで指定された比率で 2 つの色をブレンドします。
ms.openlocfilehash: 0a231954370416be201183026424c79942204e12
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432787"
---
# <a name="blend-function"></a>BLEND 関数

float パラメーターで指定された比率で 2 つの色  _をブレンド_ します。 
  
## <a name="syntax"></a>構文

BLEND(** *color1* **, ** *color2* **, ** *float[0,1]* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _color1_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |最初の色の Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _color2_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |2 番目の色の Visio カラー インデックスまたは RGB 値を指定します。  <br/> |
| _float[0,1]_ <br/> |必須  <br/> |**Float** <br/> |color2 と  _color1_ をそれぞれブレンド  _する_ 比率。 0 ～ 1 の実数を使用します。  <br/> |
   
### <a name="return-value"></a>戻り値

 **RGB**
  
## <a name="remarks"></a>注釈

返される色は、float パラメーターで指定された色  _2_ と  _色 1_ をそれぞれブレンドする相対的な比率  _によって決_ まります。 たとえば  _、float_ が 0.25 の場合、返される色は  _color1_ の 75% と  _color2_ の 25% で構成されます。 
  
もう 1 つの考え方は、  _浮動小数点_ 値が  _color1_ から color2 の色スペクトルに沿った点に対応  _する点です_。 したがって、浮動小数点数の小さい数値 (ゼロに近い) は色 _1_ に近いブレンドを生成し、より大きな数値 (1 に近い) は _color2_ に近いブレンドを生成します。
  

