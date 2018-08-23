---
title: '[TextBkgnd] セル ([Text Block Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251267
localization_priority: Normal
ms.assetid: a238bf1c-1acd-eacd-22f3-a48acaaa4549
description: 図形のテキストの背景色を指定します。
ms.openlocfilehash: 2256a4c89812924af820c020c225f4b82b1d4856
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806641"
---
# <a name="textbkgnd-cell-text-block-format-section"></a>[TextBkgnd] セル ([テキスト ブロックの書式設定] セクション)

図形のテキストの背景色を指定します。
  
## <a name="remarks"></a>注釈

[Textbkgnd] セルには、0 から 24、または 255 までの任意の値を持つことができます。 値 0 および 255 ( *visTxtBlklOpaque*) は、透明なテキストの背景を指定します。 
  
独自の色を入力するには、RGB または HSL 関数に 1 を加算を使用して、-、たとえば RGB (255, 127,255) +1 です。 独自の色の値はその RGB カラーで、し、[シェイプ シート] ウィンドウで、数値ではなく RGB ( *r, g, b*) +1 が表示されます。 数値演算で使用する場合は、25 以上の値があるユーザー設定の色です。 
  
テキストの背景色の透過性は [TextBkgndTrans] セルで設定できます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [TextBkgnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[Textbkgnd]  <br/> |
   
プログラムから、インデックスによって [TextBkgnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowText** <br/> |
|セル インデックス:  <br/> |**visTxtBlkBkgnd** <br/> |
   

