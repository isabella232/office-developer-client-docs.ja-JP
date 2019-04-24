---
title: ANGLEALONGPATH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d7f8ca9a-3a89-abab-9805-bd1e24075c3f
description: 指定されたポイントのパスに対する接線の角度を返します。
ms.openlocfilehash: 0d38fc0e123a7e38b7826b55415cfc09c1789c0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341420"
---
# <a name="anglealongpath-function"></a>ANGLEALONGPATH 関数

指定されたポイントのパスに対する接線の角度を返します。
  
## <a name="version-information"></a>バージョン情報

追加バージョン: Visio 2010
 
  
## <a name="syntax"></a>構文

ANGLEALONGPATH (* **セクション** *、* **トラベル** * * * *[, segment]* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _セクション_ <br/> |必須  <br/> |**String** <br/> |パスを表す [Geometry] セクション。[Path] セルへの参照によって指定されます (Geometry1.Path など)。  <br/> |
| _travel_ <br/> |必須  <br/> |**Double** <br/> |パスの始点から終点までの割合。 0 ～ 1 の値を指定する必要があります。  <br/> |
| _化_ <br/> |省略可能  <br/> |**整数型 (Integer)** <br/> |接線角度を計算するパスの 1 から始まるセグメント。  <br/> |
   
### <a name="return-value"></a>戻り値

 **倍精度浮動小数点型 (Double)**
  
## <a name="remarks"></a>解説

_セグメント_値を指定すると、ANGLEALONGPATH はそのセグメントの値のみを返します。 
  
_セグメント_値を指定すると、ANGLEALONGPATH は、_トラベル_を使用して、_セグメント_に沿った segment を計算することで、正接の点を決定します。
  
_section_または_segment_のいずれかが存在しない場合は、#REF! が返されます。 
  

