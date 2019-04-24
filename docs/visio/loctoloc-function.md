---
title: LOCTOLOC 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251586
localization_priority: Normal
ms.assetid: 1f09482a-0b1b-1bef-bc23-7f7793c4c65f
description: 変換後の座標系のローカル座標に変換された点を返します。
ms.openlocfilehash: f08feb6137c3022027d19b45f06285fb8b6441a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358038"
---
# <a name="loctoloc-function"></a>LOCTOLOC 関数

変換後の座標系のローカル座標に変換された点を返します。
  
## <a name="syntax"></a>構文

loctoloc (* * *srcpoint* * *, * * *srcref* * *, * * *dstref* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srcpoint_ <br/> |必須  <br/> |**String** <br/> | 変換元の座標系でのローカル座標の点を指定します。  <br/> |
| _srcref_ <br/> |必須  <br/> |**String** <br/> | 変換元オブジェクトのセルに対する参照を指定します。  <br/> |
| _dstref_ <br/> |必須  <br/> |**String** <br/> | 変換先オブジェクトのセルに対する参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

LOCTOLOC 関数は、変換元図形のローカル座標の点を、変換先図形のローカル座標に変換します。この関数を使用すると、別の座標空間の点に基づいて図形を作成できます。またローカルな点をページ座標に変換したり、ページ座標をローカルな点に変換することもできます。
  
変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。
  
変換元図形と変換先図形の座標は、同じページ上になければなりません。
  
## <a name="example"></a>例

次の数式は、数式に関連付けられている図形のローカル Pin をページ上の点に変換します。
  
```vb
LOCTOLOC(PNT(LocPinX, LocPinY), Width, ThePage!PageWidth)
```


