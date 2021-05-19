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
description: 図形の親の座標系の点の x,y 座標を返します。
ms.openlocfilehash: 4e7517c4210db31f1c3f5dc8bf98185b6f4104aa
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414509"
---
# <a name="par-function"></a>PAR 関数

図形の親の座標系の点の  _x,y_ 座標を返します。 
  
## <a name="syntax"></a>構文

PAR(** *point* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _point_ <br/> |必須  <br/> |**数値型 (Number),数値型 (Number)** <br/> |現在の図形の座標系にある点の座標を指定します。  <br/> |
   
## <a name="remarks"></a>注釈

Microsoft Visioポイントは *、x* 座標と y 座標のペアを表す *1 つの* 値です。 図形がグループに含まれる場合、その親はグループになります。 図形がグループに含まれない場合、その親はページになります。 
  
## <a name="example"></a>例

PAR(PNT(PinX,PinY)) 
  
この式では、PNT 関数によって現在の図形内にある座標の組み合わせが点に変換されます。次に PAR によって、この点が、現在の図形を含んでいるページまたはグループの左下隅を基準にした座標の組み合わせに変換されます。 
  

