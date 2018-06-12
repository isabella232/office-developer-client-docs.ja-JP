---
title: ANGLETOPAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253218
localization_priority: Normal
ms.assetid: 4d87313a-c09a-582c-04f4-d95800e3e9f2
description: 変換先図形の親座標系に変換された角度を返します。 角度を接続元の図形のローカル座標から変換先図形の親座標に変換します。
ms.openlocfilehash: 3a739c55d568dc548f8175b56f22e6ec4c28e4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804785"
---
# <a name="angletopar-function"></a>ANGLETOPAR 関数

変換先図形の親座標系に変換された角度を返します。 角度を接続元の図形のローカル座標から変換先図形の親座標に変換します。 
  
## <a name="syntax"></a>構文

ANGLETOPAR (* * *srcAngle* * *、* * *srcRef* * *、* * *dstRef* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srcAngle_ <br/> |必須  <br/> |**数値** <br/> |変換元座標系での角度を指定します。  <br/> |
| _srcRef_ <br/> |必須  <br/> |**文字列型 (String)** <br/> | 図形、グループ、ページなどの変換元オブジェクトのセルに対する参照を指定します。  <br/> |
| _dstRef_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |図形、グループ、ページなどの変換先オブジェクトのセルに対する参照を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。
  
変換元図形と変換先図形の座標は、同じページ上になければなりません。
  
変換先がページで、親図形がない場合、ページのローカル座標で結果が表示されます。
  

