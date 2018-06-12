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
ms.openlocfilehash: 942ccee4478c87243207d8d65785857758d2a068
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806648"
---
# <a name="thetext-cell-events-section"></a>[TheText] セル ([Events] セクション)

図形のテキストまたはテキストの構成が変更されたときに評価されるイベント セルです。
  
## <a name="remarks"></a>備考

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。[TheText] セルを使用して、再計算をトリガーできます。たとえば TEXTWIDTH( ) および TEXTHEIGHT( ) 関数を使用してテキストの幅と高さを再計算できます。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [thetext] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | テキスト  <br/> |
   
プログラムから、インデックスによって [thetext] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellTheText** <br/> |
   

