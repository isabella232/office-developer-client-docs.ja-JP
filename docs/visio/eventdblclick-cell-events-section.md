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
ms.openlocfilehash: a50e88ecd8e432629e246f7038dfcc9626725cc5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337171"
---
# <a name="eventdblclick-cell-events-section"></a>[EventDblClick] セル ([Events] セクション)

図形をダブルクリックしたときに評価されるイベント セルです。
  
## <a name="remarks"></a>解説

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventDblClick] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | eventdblclick]  <br/> |
   
プログラムから、インデックスによって [EventDblClick] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellDblClick** <br/> |
   

