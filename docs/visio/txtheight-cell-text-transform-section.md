---
title: '[TxtHeight] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1025
localization_priority: Normal
ms.assetid: cfa3ecc6-61a8-506c-ba1d-b5e1f757d44f
description: テキスト ブロックの高さを指定します。既定の数式は次のとおりです。
ms.openlocfilehash: e9495eef837a61fa9b7ecb2b242fdabc5df30080
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806703"
---
# <a name="txtheight-cell-text-transform-section"></a>[TxtHeight] セル ([テキスト変換] セクション)

テキスト ブロックの高さを指定します。既定の数式は次のとおりです。
  
= 高さ\*1
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtHeight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Txtheight]  <br/> |
   
プログラムから、インデックスによって [TxtHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormHeight** <br/> |
   

