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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332271"
---
# <a name="textwidth-function"></a>TEXTWIDTH 関数

図形内の構成されたテキストの幅を返します。 
  
## <a name="syntax"></a>構文

TEXTWIDTH (* * 図形の場合) ** テキスト * * * * *[, maximumwidth]* * *) 
  
### <a name="parameters"></a>パラメーター

|**名前**|**必須 / オプション**|**データ型**|**説明**|
|:-----|:-----|:-----|:-----|
| _offename! テキスト_ <br/> |必須  <br/> |**String** <br/> |ターゲットとなる図形の [TheText] セルに対する参照を指定します。  _shapename!_ は、テキストを取得する図形の名前です。  <br/> |
| _maximumwidth_ <br/> |省略可能  <br/> |**数値型 (Numeric)** <br/> |テキスト ブロックの最大幅を指定します。  <br/> |
   
### <a name="return-value"></a>戻り値

文字列
  
## <a name="remarks"></a>注釈

TEXTWIDTH 関数は、通常、格納するテキストのサイズに合わせて図形の幅を調整する場合に使用します。
  
_\n_ を省略すると、既定の図形は現在の図形になります。 
  
_maximumwidth_が指定されている場合、結果は、 _maximumwidth_に収まる最大のテキスト行になります。 _maximumwidth_を省略すると、結果はテキストの幅の合計になります。 
  
## <a name="example"></a>例

TEXTWIDTH (テキスト) 
  
現在の図形内にあるテキストの長さの合計を返します。 
  

