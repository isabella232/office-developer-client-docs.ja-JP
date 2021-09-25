---
title: '[EventXFMod] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
ms.localizationpriority: medium
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: ページ上の図形の位置または向きが変換 (XF) された場合に評価されるイベント セル。
ms.openlocfilehash: 2a8a3fd8fdb4095ebf8f5e51ed03cac1b7b060ae
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559851"
---
# <a name="eventxfmod-cell-events-section"></a>[EventXFMod] セル ([Events] セクション)

ページ上で、図形の位置または向きの変更 ("XF") が行われたときに評価されるイベント セルです。
  
## <a name="remarks"></a>注釈

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EventXFMod] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | EventXFMod  <br/> |
   
プログラムから、インデックスによって [EventXFMod] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellXFMod** <br/> |
   

