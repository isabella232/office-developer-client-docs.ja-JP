---
title: ANGLEALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: 指定されたポイントのパスに対する接線の角度を返します。
ms.openlocfilehash: a15e45ff6135972cd1cd78382147a493f8fc8d69
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160294"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH 関数

指定されたポイントのパスに対する接線の角度を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

ANGLEALONGPATH(***セクション***, ***travel*** ***[,segment]*** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セクション_ <br/> |必須  <br/> |**String** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _旅行_ <br/> |必須  <br/> |**Double** <br/> |パスの始点から終点までの割合。0 ～ 1 の値を指定する必要があります。  <br/> |
| _segment_ <br/> |省略可能  <br/> |**整数型 (Integer)** <br/> |接線角度を計算するパスの 1 から始まるセグメント。  <br/> |
   
### <a name="return-value"></a>戻り値

 **倍精度浮動小数点型 (Double)**
  
## <a name="remarks"></a>注釈

セグメント値を含  _める場合_ 、ANGLEALONGPATH は、そのセグメントの値のみを返します。 
  
セグメント値を含 _める場合_、ANGLEALONGPATH は、セグメントに沿ったパーサータージュを計算するために移動を使用して接線のポイントを決定 _します_。
  
セクションまたは _セグメント_ が _存在_ しない場合は、Microsoft Visio返#REF!。 
  

