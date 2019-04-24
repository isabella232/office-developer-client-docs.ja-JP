---
title: LOCTOPAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251585
localization_priority: Normal
ms.assetid: ce1028d6-0293-e8dd-b79d-3f02c50f6250
description: 変換後の座標系の親座標の点を返します。
ms.openlocfilehash: 65a08837d7d026836ebc8d5e35938ea049d005e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314848"
---
# <a name="loctopar-function"></a>LOCTOPAR 関数

変換後の座標系の親座標の点を返します。
  
## <a name="syntax"></a>構文

loctopar (* * *srcpoint* * *, * * *srcref* * *, * * *dstref* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _srcpoint_ <br/> |必須  <br/> |**String** <br/> | 変換元の座標系でのローカル座標の点を指定します。  <br/> |
| _srcref_ <br/> |必須  <br/> |**String** <br/> | 変換元オブジェクトのセルに対する参照を指定します。  <br/> |
| _dstref_ <br/> |必須  <br/> |**String** <br/> | 変換先オブジェクトのセルに対する参照を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

変換元図形のローカル座標から変換先図形の親座標に、点が変換されます。LOCTOPAR 関数を使用すると、別の座標系にある別の点に基づいて、図形の [PinX]、[PinY]、[BeginX]、[BeginY] などのセルに親図形の座標を設定できます。 
  
変換元図形と変換先図形がグループ内にある場合でも、この関数は機能します。変換の過程で、回転と反転についても調整されます。 
  
変換元図形と変換先図形の座標は、同じページ上になければなりません。 
  
変換先がページで、親図形がない場合、ページのローカル座標で結果が表示されます。 
  
## <a name="example"></a>例

LOCTOPAR(PNT(LocPinX, LocPinY), Width, Sheet.4!Width) 
  
数式に関連付けられている図形のローカル Pin を Sheet.4 の親座標に変換します。 
  

