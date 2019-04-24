---
title: DISTTOPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: 指定した座標で表される点からパス上の点までの最短距離を返します。
ms.openlocfilehash: 5727b24739705d3e562150c48fe77f7ad6eedb57
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332691"
---
# <a name="disttopath-function"></a>DISTTOPATH 関数

指定した座標で表される点からパス上の点までの最短距離を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

disttopath (* * *section* * *, * * *x* * *, * * *y* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セクション_ <br/> |必須  <br/> |**String** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _x_ <br/> |必須  <br/> |**Double** <br/> |点の_x_座標を指定します。  <br/> |
| _y_ <br/> |必須  <br/> |**Double** <br/> |点の_y_座標です。  <br/> |
   
### <a name="return-value"></a>戻り値

 **倍精度浮動小数点型 (Double)**
  
## <a name="remarks"></a>解説

section が存在しない場合、#REF! _セクション_が存在しない場合。 
  
戻り値は、点がトラベルの方向の左側にある場合は正、右側にある場合は負になります。
  

