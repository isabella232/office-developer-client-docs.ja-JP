---
title: RECTSECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
ms.localizationpriority: medium
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: x と y に関連付けられた四角形のセクターを計算し、セクターを示す 0 ~ 4 の整数を返します。
ms.openlocfilehash: 73e7e3aa440d67eed2a6a2706321092ec101cfdf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59607914"
---
# <a name="rectsect-function"></a>RECTSECT 関数

*x* と *y* に関連付けられた四角形のセクターを計算し、セクターを示す 0 ~ 4 の整数を返します。 
  
## <a name="syntax"></a>構文

RECTSECT(***width** _, _*_height_*_, _*_x_*_, _*_y_*_, _ *_option_** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |必須  <br/> |**String** <br/> |四角形の幅を指定します。  <br/> |
| _height_ <br/> |必須  <br/> |**String** <br/> |四角形の高さを指定します。  <br/> |
| _x_ <br/> |必須  <br/> |**String** <br/> |x 座標を指定します。  <br/> |
| _y_ <br/> |必須  <br/> |**String** <br/> |y 座標を指定します。  <br/> |
| _option_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |対角線上の点の処理方法を指定します。対角線上の点に対して左右のセクターを使用するには、値を 0 に設定します。対角線上の点に対して上下のセクターを使用するには、値を 1 に設定します。  <br/> |
   
## <a name="remarks"></a>注釈

幅と高さを持つ四角形と、四角形の中心点からの点 (*x,y*) を考えてください。 四角形の角を結ぶ対角線を描画し、四角形を 4 つのセクターに分割して、中心点を示します。 セクター 0 ～ 4 は、それぞれ中心点、右、上、左、下を表します。 
  
![セクター 0 ~ 4 は、それぞれ中心点、右、上、左、および下を表します。](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>例

RECTSECT(1 in, 2 in, 1 in, -7 in, 0) 
  
4 を返します。 
  

