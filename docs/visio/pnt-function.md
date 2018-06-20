---
title: PNT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251480
localization_priority: Normal
ms.assetid: d14a735c-0278-922f-7823-79adf6cb1e64
description: 座標で表される点を返します。 x および y 値を 1 つにします。
ms.openlocfilehash: be00f7d5ae55f70407e35eca43881a6d3f70ec13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806065"
---
# <a name="pnt-function"></a>PNT 関数

座標_x_と_y_を 1 つの値で表される点を返します。 
  
## <a name="syntax"></a>構文

Pnt 関数 (* * *x y* * *) 
  
### <a name="parameters"></a>Parameters

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _x, y_ <br/> |必須  <br/> |**番号** <br/> |現在の図形の座標系にある点の座標を指定します。  <br/> |
   
### <a name="return-value"></a>�߂�l

点
  
## <a name="remarks"></a>注釈

ポイントに座標を変換すると、 *x*および*y*を操作しなくても図形座標を変更するのには、座標を別々 にします。 
  
## <a name="example"></a>例

PNT(PinX,PinY) 
  
[PinX] と [PinY] で表される点を返します。 
  

