---
title: '[EventDblClick] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
localization_priority: Normal
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: 図形をダブルクリックしたときに評価されるイベント セルです。
ms.openlocfilehash: 623d1d095d3269cd9c82fa8d0d6601933a163f92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805323"
---
# <a name="eventdblclick-cell-events-section"></a>[EventDblClick] セル ([Events] セクション)

図形をダブルクリックしたときに評価されるイベント セルです。
  
## <a name="remarks"></a>備考

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって EventDblClick] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | EventDblClick  <br/> |
   
プログラムから、インデックスによって [EventDblClick] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellDblClick** <br/> |
   

