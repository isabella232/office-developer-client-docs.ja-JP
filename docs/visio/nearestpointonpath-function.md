---
title: NEARESTPOINTONPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 539bf79a-df09-2048-2aba-8c863dd26fc2
description: 指定した座標に最も近い点のパスに沿った距離の割合を、0 ～ 1 の値として返します。
ms.openlocfilehash: d9e9b890033526fec99f04cee30ae93578487652
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805912"
---
# <a name="nearestpointonpath-function"></a>NEARESTPOINTONPATH 関数

指定した座標に最も近い点のパスに沿った距離の割合を、0 ～ 1 の値として返します。
  
## <a name="version-information"></a>バージョン情報

Visio 2010 のバージョンが追加されます。 
  
## <a name="syntax"></a>構文

NEARESTPOINTONPATH (* **で** *、* * *x* * *、* * *y* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _x_ <br/> |必須  <br/> |**Double** <br/> |_X_で指定された点の座標です。  <br/> |
| _y_ <br/> |必須  <br/> |**Double** <br/> |_Y_で指定された点の座標です。  <br/> |
   
### <a name="return-value"></a>�߂�l

 **Double**
  
## <a name="remarks"></a>解説

_セクション_が存在しない場合 Microsoft Visio は #ref! を返します。 
  

