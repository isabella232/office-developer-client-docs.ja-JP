---
title: '[TxtLocPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251276
ms.localizationpriority: medium
ms.assetid: 3f46cfcf-7eac-4a37-e782-39f4e7f8fc43
description: テキスト ブロックの原点を基準に、テキスト ブロックの回転中心の y 座標を指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: 745a067a6ac7aca50e2bd2789fb9951bc96e2595
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627248"
---
# <a name="txtlocpiny-cell-text-transform-section"></a>[TxtLocPinY] セル ([Text Transform] セクション)

テキスト ブロックの原点を基準に、テキスト ブロックの回転中心の  *y*  座標を指定します。 既定の数式は次のとおりです。 
  
= TxtHeight \* 0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtLocPinY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtLocPinY  <br/> |
   
プログラムから、インデックスによって [TxtLocPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormLocPinY** <br/> |
   

