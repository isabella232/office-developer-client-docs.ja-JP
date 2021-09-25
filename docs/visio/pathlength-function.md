---
title: PATHLENGTH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: 指定した [Geometry] セクションで定義されているパスの長さを返します。
ms.openlocfilehash: da00d0b144be5526eaa8d253b7b52a397af68538
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608072"
---
# <a name="pathlength-function"></a>PATHLENGTH 関数

指定した [Geometry] セクションで定義されているパスの長さを返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

PATHLENGTH(** *section* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セクション_ <br/> |必須  <br/> |**String** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _segment_ <br/> |省略可能  <br/> |**整数型 (Integer)** <br/> |測定するパスの 1 から始まるセグメント。  <br/> |
   
### <a name="return-value"></a>戻り値

 **倍精度浮動小数点型 (Double)**
  
## <a name="remarks"></a>注釈

セクション _または_ セグメント _が存在_ しない場合、Microsoft Visioが#REF! 
  
セグメント値を含  _める場合_ 、PATHLENGTH はセグメントの長さを返します。 
  

