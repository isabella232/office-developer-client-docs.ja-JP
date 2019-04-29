---
title: '[FillBkgnd] セル ([Fill Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm365
localization_priority: Normal
ms.assetid: 603d698f-a025-538c-8767-18e7716a9a5f
description: 図形の塗りつぶしのパターンで背景に使用する色 (塗りつぶし部分) を指定します。
ms.openlocfilehash: f4df5d2b44a50380c996b9b2e0f7cda7d212093b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436644"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>[FillBkgnd] セル ([Fill Format] セクション)

図形の塗りつぶしのパターンで背景に使用する色 (塗りつぶし部分) を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、0 ～ 23 の数値を入力します。
  
ユーザー設定の色を入力するには、RGB または HSL 関数を使用します。ユーザー設定の色の値はその RGB カラーで示され、番号ではなく RGB(*r, g, b*) が [シェイプシート] ウィンドウに表示されます。ユーザー設定の色を数値演算で使用する場合は、24 以上の値を指定します。 
  
背景の塗りつぶしの色に関する透過性を設定するには、[FillBkgndTrans] セルを使用します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [FillBkgnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [fillbkgnd]  <br/> |
   
プログラムから、インデックスによって [FillBkgnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillBkgnd** <br/> |
   

