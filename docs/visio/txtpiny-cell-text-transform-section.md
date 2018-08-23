---
title: '[TxtPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
localization_priority: Normal
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: Y の決定に、テキスト ブロックの図形の原点を基準として回転の中心の座標。 既定の数式は次のとおりです。
ms.openlocfilehash: e8101463413b177bf8ddd80ed52964d3eeae788f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806707"
---
# <a name="txtpiny-cell-text-transform-section"></a>[TxtPinY] セル ([テキスト変換] セクション)

*Y*の決定に、テキスト ブロックの図形の原点を基準として回転の中心の座標。 既定の数式は次のとおりです。 
  
= 高さ\*0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtPinY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Txtpiny]  <br/> |
   
プログラムから、インデックスによって [TxtPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormPinY** <br/> |
   

