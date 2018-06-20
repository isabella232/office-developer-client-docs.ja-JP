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
description: 親図形の座標系の x、点の y 座標を返します。
ms.openlocfilehash: a3f7afd3f9bc988a20526451a6d7d7081d27a2d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805975"
---
# <a name="par-function"></a>PAR 関数

親図形の座標系の点の_x, y_座標を返します。 
  
## <a name="syntax"></a>構文

額面価格 (* **ポイント** *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _ポイント_ <br/> |必須  <br/> |**番号** <br/> |現在の図形の座標系にある点の座標を指定します。  <br/> |
   
## <a name="remarks"></a>備考

Microsoft Visio で、ポイントは、 *x*および*y*のペアを具体化した単一の値の座標です。 図形がグループ内にある場合は、その親はグループです。 図形がグループ内にない場合は、その親はページです。 
  
## <a name="example"></a>例

PAR(PNT(PinX,PinY)) 
  
この式では、PNT 関数によって現在の図形内にある座標の組み合わせが点に変換されます。次に PAR によって、この点が、現在の図形を含んでいるページまたはグループの左下隅を基準にした座標の組み合わせに変換されます。 
  

