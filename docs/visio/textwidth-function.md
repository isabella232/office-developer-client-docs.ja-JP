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
description: 図形で構成されたテキストの幅を返します。
ms.openlocfilehash: d96b9489c08ce38205f8e9ad91e361fcb643c39c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806627"
---
# <a name="textwidth-function"></a>TEXTWIDTH 関数

図形で構成されたテキストの幅を返します。 
  
## <a name="syntax"></a>構文

TEXTWIDTH (* **なります。[Thetext]* * * * * *[] maximumwidth* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _なります! テキスト_ <br/> |必須  <br/> |**文字列型 (String)** <br/> |セルへの参照では、接続先の図形の [thetext] という名前です。  _なります!_ テキストを取得する図形の名前です。  <br/> |
| _maximumwidth_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |テキスト ブロックの最大幅を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

String
  
## <a name="remarks"></a>注釈

TEXTWIDTH 関数は、通常、格納するテキストのサイズに合わせて図形の幅を調整する場合に使用します。
  
場合_sheetN!_ 省略すると、現在の図形は、オートシェイプの既定値です。 
  
_Maximumwidth_が指定されている場合は_maximumwidth_内に収まっているテキストの最長の行になります。 _Maximumwidth_を省略すると、テキストの幅の合計になります。 
  
## <a name="example"></a>例

TEXTWIDTH(TheText) 
  
現在の図形内にあるテキストの長さの合計を返します。 
  

