---
title: '[EventDrop] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm350
localization_priority: Normal
ms.assetid: f84afe83-8391-0c13-f442-ea8794b38642
description: 図面ページに図形をインスタンスとしてドロップしたとき、または図形を複製したり貼り付けたときに評価されるイベント セルです。
ms.openlocfilehash: e2624c50896de061727003a48f7dc1559c6a72c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805321"
---
# <a name="eventdrop-cell-events-section"></a>[EventDrop] セル ([イベント] セクション)

図面ページに図形をインスタンスとしてドロップしたとき、または図形を複製したり貼り付けたときに評価されるイベント セルです。
  
## <a name="remarks"></a>備考

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventDrop] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [Eventdrop]  <br/> |
   
プログラムから、インデックスによって [EventDrop] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellDrop** <br/> |
   

