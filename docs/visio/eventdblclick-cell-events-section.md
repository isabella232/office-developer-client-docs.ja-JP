---
title: '[EventDblClick] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251312
ms.localizationpriority: medium
ms.assetid: ca949013-f998-1bce-39e5-ac6f68ab2392
description: 図形をダブルクリックしたときに評価されるイベント セルです。
ms.openlocfilehash: 7e3fc2568d4afbeb041057aa78790953a2357acc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619078"
---
# <a name="eventdblclick-cell-events-section"></a>[EventDblClick] セル ([Events] セクション)

図形をダブルクリックしたときに評価されるイベント セルです。
  
## <a name="remarks"></a>注釈

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventDblClick] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | EventDblClick  <br/> |
   
プログラムから、インデックスによって [EventDblClick] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellDblClick** <br/> |
   

