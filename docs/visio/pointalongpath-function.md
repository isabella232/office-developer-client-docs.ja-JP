---
title: POINTALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7f91e5d9-89b8-5a0d-e01f-aa81fbd5e1fd
description: パスの点またはパスからのオフセットの座標を返します。
ms.openlocfilehash: ce8b54bbd821cbfa6eb1f2789193ff8d7dda42d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430484"
---
# <a name="pointalongpath-function"></a>POINTALONGPATH 関数

パスの点またはパスからのオフセットの座標を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

POINTALONGPATH(** *section* **, ** *travel* ** *[,offset]* ** ** *[,segment]* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セクション_ <br/> |必須  <br/> |**String** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _旅行_ <br/> |必須  <br/> |**Double** <br/> |点を識別する、スキャンするパスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。  <br/> |
| _offset_ <br/> |省略可能  <br/> |**倍精度浮動小数点型 (Double)** <br/> |点がパスからオフセットする距離。詳細については、「備考」を参照してください。  <br/> |
| _segment_ <br/> |省略可能  <br/> |**整数型 (Integer)** <br/> |座標を計算するパスの 1 から始まるセグメント。  <br/> |
   
### <a name="return-value"></a>戻り値

 **Point**
  
## <a name="remarks"></a>注釈

セクション _または_ セグメント _が存在_ しない場合、Microsoft Visioが#REF! 
  
正  *のオフセット*  値は、移動方向の左側のポイントを指定します。 
  
負  *のオフセット*  値は、移動方向の右側のポイントを指定します。 
  
**Point** は、図形座標 (*x,y*) の整列されたペアを 1 つの値として表します。 
  

