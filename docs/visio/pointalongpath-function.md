---
title: POINTALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: パスの点またはパスからのオフセットの座標を返します。
ms.openlocfilehash: 9ce6f8c171515b46aaff0ce07cbe7da4f1e958d9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806021"
---
# <a name="pointalongpath-function"></a>POINTALONGPATH 関数

パスの点またはパスからのオフセットの座標を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

POINTALONGPATH (* **で** *、* **旅行** * * * *[] オフセット** * * * *[] セグメント** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _section_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _旅行_ <br/> |必須  <br/> |**Double** <br/> |点を識別する、スキャンするパスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。  <br/> |
| _オフセット_ <br/> |省略可能  <br/> |**倍精度浮動小数点型 (Double)** <br/> |点がパスからオフセットする距離。詳細については、「備考」を参照してください。  <br/> |
| _セグメント_ <br/> |省略可能  <br/> |**整数型 (Integer)** <br/> |座標を計算するパスの 1 から始まるセグメント。  <br/> |
   
### <a name="return-value"></a>戻り値

 **点**
  
## <a name="remarks"></a>注釈

_セクション_または_セグメント_が存在しない場合 Microsoft Visio は #ref! を返します。 
  
正の*オフセット*値では、旅行の方向の左へのポインターを指定します。 
  
負の*オフセット*値では、旅行の方向の右へのポインターを指定します。 
  
**Point** は、図形座標 (*x,y*) の整列されたペアを 1 つの値として表します。 
  

