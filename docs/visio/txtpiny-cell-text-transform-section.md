---
title: '[TxtPinY] セル ([Text Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1045
ms.localizationpriority: medium
ms.assetid: 88ddf4b5-8248-8c1a-c387-09a607639d26
description: 図形の原点に対するテキスト ブロックの回転中心の y 座標を指定します。 既定の数式は次のとおりです。
ms.openlocfilehash: a08e1da3a7e36cf7bfd04d199a949dfe91d6df33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603236"
---
# <a name="txtpiny-cell-text-transform-section"></a>[TxtPinY] セル ([Text Transform] セクション)

図形の原点に対するテキスト ブロックの回転中心の  *y*  座標を指定します。 既定の数式は次のとおりです。 
  
= 高 \* さ 0.5
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TxtPinY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | TxtPinY  <br/> |
   
プログラムから、インデックスによって [TxtPinY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス :  <br/> |**visRowTextXForm** <br/> |
| セル インデックス:  <br/> |**visXFormPinY** <br/> |
   

