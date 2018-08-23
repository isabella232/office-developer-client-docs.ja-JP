---
title: '[TxtAngle] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251272
localization_priority: Normal
ms.assetid: b8482cd8-5205-40ef-b4e1-4ceb197ac80f
description: テキスト ブロックの現在の x を基準にして回転角度を指定の形状の軸です。 既定値は、0 度です。
ms.openlocfilehash: 08ed4422392a355db948fa947abdfd3772dec0a9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806695"
---
# <a name="txtangle-cell-text-transform-section"></a>[TxtAngle] セル ([テキスト変換] セクション)

テキスト ブロックの現在の*x*を基準にして回転角度を指定の形状の軸です。 既定値は、0 度です。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtAngle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Txtangle]  <br/> |
   
プログラムから、インデックスによって [TxtAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormAngle** <br/> |
   

