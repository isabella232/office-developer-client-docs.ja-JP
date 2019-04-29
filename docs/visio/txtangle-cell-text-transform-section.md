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
description: 図形の x 軸を基準として、テキストブロックの現在の回転角度を指定します。 既定値は 0°です。
ms.openlocfilehash: 701a2b0ce5fccb29cc61309de1d1768a96d92c99
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432171"
---
# <a name="txtangle-cell-text-transform-section"></a>[TxtAngle] セル ([Text Transform] セクション)

図形の*x*軸を基準として、テキストブロックの現在の回転角度を指定します。 既定値は 0°です。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtAngle] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [txtangle]  <br/> |
   
プログラムから、インデックスによって [TxtAngle] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormAngle** <br/> |
   

