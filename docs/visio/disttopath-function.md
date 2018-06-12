---
title: DISTTOPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ba7d372-0c2a-9fa7-0af6-97da0aafdb12
description: 指定した座標で表される点からパス上の点までの最短距離を返します。
ms.openlocfilehash: 227fe860de2e3683b5d7d3e5f9313d1e2e31b2d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805255"
---
# <a name="disttopath-function"></a>DISTTOPATH 関数

指定した座標で表される点からパス上の点までの最短距離を返します。
  
## <a name="version-information"></a>バージョン情報

Visio 2010 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

DISTTOPATH (* **で** *、* * *x* * *、* * *y* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _x_ <br/> |必須  <br/> |**Double** <br/> |_X_-点の座標です。  <br/> |
| _y_ <br/> |必須  <br/> |**Double** <br/> |_Y_-点の座標です。  <br/> |
   
### <a name="return-value"></a>�߂�l

 **Double**
  
## <a name="remarks"></a>解説

Microsoft Visio では、#REF を返す! _セクション_が存在しません。 場合、 
  
戻り値は、点がトラベルの方向の左側にある場合は正、右側にある場合は負になります。
  

