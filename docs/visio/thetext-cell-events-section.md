---
title: '[TheText] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm1005
localization_priority: Normal
ms.assetid: 2d63768e-afdb-4b3f-de49-f9ba69ae5391
description: 図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。
ms.openlocfilehash: 6aa5e14f339d0030d8421eaae62b0e481be91fc7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435167"
---
# <a name="thetext-cell-events-section"></a>[TheText] セル ([Events] セクション)

図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。
  
## <a name="remarks"></a>注釈

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。[TheText] セルを使用して、再計算をトリガーできます。たとえば TEXTWIDTH( ) および TEXTHEIGHT( ) 関数を使用してテキストの幅と高さを再計算できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TheText] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [thetext]  <br/> |
   
プログラムから、インデックスによって [TheText] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellTheText** <br/> |
   

