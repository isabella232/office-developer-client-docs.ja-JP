---
title: '[PinY] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm795
localization_priority: Normal
ms.assetid: 98b86b9d-9cc0-1169-1c44-ef1505bf92fa
description: 親図形の原点を基準としたときの、図形の pin (回転の中心) の y 座標を表します。
ms.openlocfilehash: 17daf691e4802a93775bfd5272d2142ef33bd189
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411863"
---
# <a name="piny-cell-shape-transform-section"></a>[PinY] セル ([Shape Transform] セクション)

親図形の原点を基準としたときの、図形の pin (回転の中心) の*y*座標を表します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PinY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PinY  <br/> |
   
プログラムから、インデックスによって [PinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormPinY** <br/> |
   

