---
title: '[EventMultiDrop] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: 35d38657048b65263fd932e540d2ca15e8006be2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582730"
---
# <a name="eventmultidrop-cell-events-section"></a>[EventMultiDrop] セル ([Events] セクション)

複数の図形が図面ページにドロップされた場合、インスタンスとして、または図形が複製または貼り付けされた場合に評価されるイベント セル。
  
イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventMultiDrop] セルを参照するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |EventMultiDrop  <br/> |
   
プログラムから、インデックスによって [EventMultiDrop] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowEvent** <br/> |
|セル インデックス:  <br/> |**visEvtCellMultiDrop** <br/> |
   

