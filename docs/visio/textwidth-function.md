---
title: TEXTWIDTH 関数
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251505
localization_priority: Normal
ms.assetid: a9b8efcf-edc0-ad99-deae-21df16c58807
description: 図形内の構成されたテキストの幅を返します。
ms.openlocfilehash: 43848bba4d24a0c31a3a084d123cd56140bf0709
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422034"
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
  

