---
title: '[TxtLocPinX] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251275
localization_priority: Normal
ms.assetid: cbfc4e91-10d1-d50e-3e8a-f269f7123276
description: X の決定に、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。 既定の数式は次のとおりです。
ms.openlocfilehash: 6eb48532bb19bce5b0d22ed2cd0997014721df88
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806690"
---
# <a name="txtlocpinx-cell-text-transform-section"></a>[TxtLocPinX] セル ([Text Transform] セクション)

*X*が決まりますが、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。 既定の数式は次のとおりです。 
  
= [Txtwidth] \* 0.5
  
この数式では、テキスト ブロックの水平方向の中心が回転の中心になります。
  
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[TxtLocPinX] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtLocPinX  <br/> |
   
プログラムから、インデックスによって [TxtLocPinX] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinX** <br/> |
   

