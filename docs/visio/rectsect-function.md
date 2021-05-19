---
title: RECTSECT 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251486
localization_priority: Normal
ms.assetid: e83343c5-df5f-bf74-f854-6380176693a2
description: x と y に関連付けられた四角形のセクターを計算し、セクターを示す 0 ~ 4 の整数を返します。
ms.openlocfilehash: 442ec0d614589c709a097ba314abad044d470df6
ms.sourcegitcommit: 41f2ee16badd6009bab642d68a61eaaccb91c3ec
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 07/17/2020
ms.locfileid: "45160273"
---
# <a name="rectsect-function"></a>RECTSECT 関数

*x* と *y* に関連付けられた四角形のセクターを計算し、セクターを示す 0 ~ 4 の整数を返します。 
  
## <a name="syntax"></a>構文

RECTSECT(***width***, ***height***, ***x***, ***y***, ***option*** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |必須  <br/> |**String** <br/> |四角形の幅を指定します。  <br/> |
| _height_ <br/> |必須  <br/> |**String** <br/> |四角形の高さを指定します。  <br/> |
| _x_ <br/> |必須  <br/> |**String** <br/> |x 座標を指定します。  <br/> |
| _y_ <br/> |必須  <br/> |**String** <br/> |y 座標を指定します。  <br/> |
| _option_ <br/> |必須  <br/> |**Boolean** <br/> |対角線上の点の処理方法を指定します。対角線上の点に対して左右のセクターを使用するには、値を 0 に設定します。対角線上の点に対して上下のセクターを使用するには、値を 1 に設定します。  <br/> |
   
## <a name="remarks"></a>注釈

幅と高さを持つ四角形と、四角形の中心点からの点 (*x,y*) を考えてください。 四角形の角を結ぶ対角線を描画し、四角形を 4 つのセクターに分割して、中心点を示します。 セクター 0 ～ 4 は、それぞれ中心点、右、上、左、下を表します。 
  
![セクター 0 ~ 4 は、それぞれ中心点、右、上、左、および下を表します。](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>例

RECTSECT(1 in, 2 in, 1 in, -7 in, 0) 
  
4 を返します。 
  

