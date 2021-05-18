---
title: PATHLENGTH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f47ea08-fb5e-7d48-e84a-2a6570564924
description: 指定した [Geometry] セクションで定義されているパスの長さを返します。
ms.openlocfilehash: e4f90c2bb886f54164bedab5f8d78fc528758414
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405850"
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
  

