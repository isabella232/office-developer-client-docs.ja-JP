---
title: '[TxtLocPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
localization_priority: Normal
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: Y が決まりますが、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。 既定の数式は次のとおりです。
ms.openlocfilehash: 7d43f63b8560df5fc5daf09a429ce30ec976d131
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806699"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>[TxtLocPinY] セル ([テキスト変換] セクション)

*Y*が決まりますが、テキスト ブロックのテキスト ブロックの原点を基準として回転の中心の座標。 既定の数式は次のとおりです。 
  
= [Txtheight] \* 0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtLocPinY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtLocPinY  <br/> |
   
プログラムから、インデックスによって [TxtLocPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinY** <br/> |
   

