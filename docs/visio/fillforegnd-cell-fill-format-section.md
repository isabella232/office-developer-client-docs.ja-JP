---
title: '[FillForegnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251241
localization_priority: Normal
ms.assetid: 7548a480-4dce-45e0-281b-f6f8bdf05c0b
description: 図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。
ms.openlocfilehash: 27126457963e4e55419b0cac5baf1eab08fe3cc6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805392"
---
# <a name="fillforegnd-cell-fill-format-section"></a>[FillForegnd] セル ([塗りつぶしの書式設定] セクション)

図形の塗りつぶしのパターンで前景 (ストローク部分) に使用する色を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、0 ～ 23 の数値を入力します。
  
独自の色を入力するには、RGB または HSL 関数を使用します。 その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB ( *r, g, b*)、[シェイプ シート] ウィンドウが表示されます。 数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。 
  
前景の塗りつぶしの色に関する透過性を設定するには、[FillForegndTrans] セルを使用します。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillForegnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |FillForegnd  <br/> |
   
プログラムから、インデックスによって [FillForegnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowFill** <br/> |
|セル インデックス:  <br/> |**visFillForegnd** <br/> |
   

