---
title: PNT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
ms.localizationpriority: medium
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: 座標 x と y で表される点を 1 つの値として返します。
ms.openlocfilehash: b6c0c9b15aa6b6fb640d433dd866e1977191f872
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573748"
---
# <a name="pnt-function"></a>PNT 関数

座標 x と y で表される点を _1_ つの値として返します。 
  
## <a name="syntax"></a>構文

PNT(** *x,y* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _x,y_ <br/> |必須かどうか  <br/> |**数値型 (Number),数値型 (Number)** <br/> |現在の図形の座標系にある点の座標を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

Point
  
## <a name="remarks"></a>注釈

座標をポイントに変換すると  *、x*  座標と  *y*  座標を個別に操作することなく、図形のジオメトリを変更できます。 
  
## <a name="example"></a>例

PNT(PinX,PinY) 
  
[PinX] と [PinY] で表される点を返します。 
  

