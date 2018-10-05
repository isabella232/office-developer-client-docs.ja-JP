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
description: X に関連付けられている四角形のセクターを計算し、y、セクターを示す 0 ~ 4 の整数を返します。
ms.openlocfilehash: fb7ed37ac498765e21c62d7180413cdbcb932502
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395085"
---
# <a name="rectsect-function"></a>RECTSECT 関数

*X*および*y*に関連付けられている四角形のセクターを計算し、セクターを示す 0 ~ 4 の整数を返します。 
  
## <a name="syntax"></a>構文

RECTSECT (* **幅** *、* **高さ** *、* * *x* * *、* * *y* * *、* **オプション** *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _width_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |四角形の幅を指定します。  <br/> |
| _height_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |四角形の高さを指定します。  <br/> |
| _x_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |x 座標を指定します。  <br/> |
| _y_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |y 座標を指定します。  <br/> |
| _オプション_ <br/> |必須  <br/> |**ブール型 (Boolean)** <br/> |対角線上の点の処理方法を指定します。対角線上の点に対して左右のセクターを使用するには、値を 0 に設定します。対角線上の点に対して上下のセクターを使用するには、値を 1 に設定します。  <br/> |
   
## <a name="remarks"></a>注釈

四角形の*幅*と*高さ*、および四角形の中心点から点 (*x, y*) を持つことを検討してください。 中心点とその 4 つのセクターに分割するのには四角形の角を結ぶ対角線を描画します。 セクター 0 から 4 までは、中心点、右、上、左を表現し、それぞれの下します。 
  
![セクター 0 から 4 までは、中心点、右、上、左を表現し、それぞれ下](media/ShpSheetRef_CA_03_ZA07645862.gif)
  
## <a name="example"></a>例

RECTSECT(1 in, 2 in, 1 in, -7 in, 0) 
  
4 を返します。 
  

