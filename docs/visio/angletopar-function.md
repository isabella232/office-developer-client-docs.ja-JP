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
description: 変換先図形の親座標系に基づいて変換された角度を返します。 つまり、変換元図形のローカル座標から変換先図形の親座標に、角度が変換されます。
ms.openlocfilehash: e411cbae21d832039e2fbda93393a8fe0bd1f9f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341456"
---
# <a name="angletopar-function"></a>ANGLETOPAR 関数

変換先図形の親座標系に基づいて変換された角度を返します。 つまり、変換元図形のローカル座標から変換先図形の親座標に、角度が変換されます。 
  
## <a name="syntax"></a>構文

ANGLETOPAR (* * *srcangle* * *、* * *srcref* * *、* * *dstref* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srcangle_ <br/> |必須  <br/> |**数値型 (Numeric)** <br/> |変換元座標系での角度を指定します。  <br/> |
| _srcref_ <br/> |必須  <br/> |**String** <br/> | 図形、グループ、ページなどの変換元オブジェクトのセルに対する参照を指定します。  <br/> |
| _dstref_ <br/> |必須  <br/> |**String** <br/> |図形、グループ、ページなどの変換先オブジェクトのセルに対する参照を指定します。  <br/> |
   
## <a name="remarks"></a>解説

変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。
  
変換元図形と変換先図形の座標は、同じページ上になければなりません。
  
変換先がページで、親図形がない場合、ページのローカル座標で結果が表示されます。
  

