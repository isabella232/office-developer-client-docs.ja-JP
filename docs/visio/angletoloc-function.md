---
title: ANGLETOLOC 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253217
ms.localizationpriority: medium
ms.assetid: ee5e3898-bb49-57c6-0ebe-12e1fe388e55
description: 変換先図形のローカル座標系に変換された角度を返します。つまり、変換元図形のローカル座標から変換先図形のローカル座標に、角度が変換されます。
ms.openlocfilehash: e223c5517b01c881367da19a8cb3c5e3f1c0780b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603929"
---
# <a name="angletoloc-function"></a>ANGLETOLOC 関数

変換先図形のローカル座標系に変換された角度を返します。つまり、変換元図形のローカル座標から変換先図形のローカル座標に、角度が変換されます。 
    
 
  
## <a name="syntax"></a>構文

ANGLETOLOC(***srcAngle** _, _*_srcRef_*_, _ *_dstRef_** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |必須かどうか  <br/> |**数値型 (Numeric)** <br/> |変換元座標系での角度を指定します。  <br/> |
| _srcRef_ <br/> |必須  <br/> |**String** <br/> | 図形、グループ、ページなどの変換元オブジェクトのセルに対する参照を指定します。  <br/> |
| _dstRef_ <br/> |必須  <br/> |**String** <br/> |図形、グループ、ページなどの変換先オブジェクトのセルに対する参照を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

ANGLETOLOC 関数を使用すると、別の座標空間の角度に基づいて、図形内にあるローカルの角度のセルを設定できます。
  
変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。
  
変換元図形と変換先図形の座標は、同じページ上になければなりません。
  

