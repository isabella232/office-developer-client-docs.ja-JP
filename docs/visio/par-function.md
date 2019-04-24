---
title: PAR 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251477
localization_priority: Normal
ms.assetid: 9caf424d-cb70-8f1a-b984-64cf776bdfb4
description: 図形の親の座標系にある点の x, y 座標を返します。
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32269945"
---
# <a name="par-function"></a>PAR 関数

図形の親の座標系にある点の_x, y_座標を返します。 
  
## <a name="syntax"></a>構文

額面 (* **ポイント** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _ポイント_ <br/> |必須  <br/> |**数値型 (Number),数値型 (Number)** <br/> |現在の図形の座標系にある点の座標を指定します。  <br/> |
   
## <a name="remarks"></a>解説

Microsoft Visio では、1つのポイントは*x*座標と*y*座標のペアを具体化した単一の値です。 図形がグループに含まれる場合、その親はグループになります。 図形がグループに含まれない場合、その親はページになります。 
  
## <a name="example"></a>例

額面 (PNT (PinX、PinY)) 
  
この式では、PNT 関数によって現在の図形内にある座標の組み合わせが点に変換されます。次に PAR によって、この点が、現在の図形を含んでいるページまたはグループの左下隅を基準にした座標の組み合わせに変換されます。 
  

