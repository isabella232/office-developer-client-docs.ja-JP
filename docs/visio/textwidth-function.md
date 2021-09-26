---
title: TEXTWIDTH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
ms.localizationpriority: medium
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: 図形内の構成されたテキストの幅を返します。
ms.openlocfilehash: 7db00c5d7d0c1e984bb18e786364569afe0ec0e0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627339"
---
# <a name="textwidth-function"></a>TEXTWIDTH 関数

図形内の構成されたテキストの幅を返します。 
  
## <a name="syntax"></a>構文

TEXTWIDTH(** *shapename!TheText* ** *** [,maximumwidth]* ** ) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _shapename!theText_ <br/> |必須  <br/> |**String** <br/> |ターゲットとなる図形の [TheText] セルに対する参照を指定します。  _shapename!_ は、テキストを取得する図形の名前です。  <br/> |
| _maximumwidth_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |テキスト ブロックの最大幅を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

TEXTWIDTH 関数は、通常、格納するテキストのサイズに合わせて図形の幅を調整する場合に使用します。
  
_sheetN!_ を省略すると、既定の図形は現在の図形になります。 
  
_maximumwidth を指定_ すると、結果は最大の範囲に収まるテキストの最長行 _になります_。 _maximumwidth を_ 省略すると、テキストの合計幅が返されます。 
  
## <a name="example"></a>例

TEXTWIDTH(TheText) 
  
現在の図形内にあるテキストの長さの合計を返します。 
  

