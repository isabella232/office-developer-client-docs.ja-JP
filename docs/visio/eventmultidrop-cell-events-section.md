---
title: '[EventMultiDrop] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: caa86e33d0d7aa9ca31cbbf8939e17b581877669
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337192"
---
# <a name="eventmultidrop-cell-events-section"></a>[EventMultiDrop] セル ([Events] セクション)

図面ページに複数の図形をインスタンスとしてドロップしたとき、または図形を複製または貼り付けたときに評価されるイベントセルです。
  
イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventMultiDrop] セルを参照するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[eventmultidrop]  <br/> |
   
プログラムから、インデックスによって [EventMultiDrop] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowEvent** <br/> |
|セル インデックス:  <br/> |**visEvtCellMultiDrop** <br/> |
   

