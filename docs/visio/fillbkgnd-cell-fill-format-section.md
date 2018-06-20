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
ms.openlocfilehash: d1222026887313d7737a3a0ded9e798e9bf5ea30
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805371"
---
# <a name="fillbkgnd-cell-fill-format-section"></a>[FillBkgnd] セル ([Fill Format] セクション)

図形の塗りつぶしのパターンで背景に使用する色 (塗りつぶし部分) を指定します。
  
## <a name="remarks"></a>注釈

色を設定するには、0 ～ 23 の数値を入力します。
  
独自の色を入力するには、RGB または HSL 関数を使用します。 その RGB カラーでは、ユーザー設定の色の値と、数値ではなく RGB (*r, g, b*)、[シェイプ シート] ウィンドウが表示されます。 数値演算で使用する場合は、24 以上の値があるユーザー設定の色です。 
  
背景の塗りつぶしの色に関する透過性を設定するには、[FillBkgndTrans] セルを使用します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [fillbkgnd] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Fillbkgnd]  <br/> |
   
プログラムから、インデックスによって [fillbkgnd] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowFill** <br/> |
| セル インデックス:  <br/> |**visFillBkgnd** <br/> |
   

