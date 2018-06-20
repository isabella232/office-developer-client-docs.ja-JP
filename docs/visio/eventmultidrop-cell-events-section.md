---
title: '[EventMultiDrop] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f496d698-7f08-69cc-4379-df18a2c2fd7e
ms.openlocfilehash: e44cd18c3f7673761f457db9cd4bfe00a8ab89bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805338"
---
# <a name="eventmultidrop-cell-events-section"></a>[EventMultiDrop] セル ([Events] セクション)

インスタンスまたはシェイプを複製したり貼り付けたときに、図面ページに複数の図形をドロップしたときに評価されるイベント セルです。
  
イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
参照してください EventMultiDrop] セルへの名前で別の数式または**CellsU**プロパティを使用したプログラムから、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |EventMultiDrop  <br/> |
   
EventMultiDrop] セルへインデックスを使用してプログラムから、参照するには、次の引数で**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowEvent** <br/> |
|セル インデックス:  <br/> |**visEvtCellMultiDrop** <br/> |
   

