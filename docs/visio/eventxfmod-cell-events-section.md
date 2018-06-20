---
title: '[EventXFMod] セル ([Events] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251313
localization_priority: Normal
ms.assetid: b88588a2-c651-7eab-9c7a-ed78f20d1ba3
description: 図形の位置や、ページの向きは、するときに評価されるイベント セルは、(XF) を変換します。
ms.openlocfilehash: 5884aabc11798ae0440fbfa024b9cc2f2418b9cc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805350"
---
# <a name="eventxfmod-cell-events-section"></a>[EventXFMod] セル ([Events] セクション)

ページ上で、図形の位置または向きの変更 ("XF") が行われたときに評価されるイベント セルです。
  
## <a name="remarks"></a>備考

イベント セルはイベントの発生時にのみ評価されます。数式の入力時には評価されません。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [eventxfmod] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Eventxfmod]  <br/> |
   
プログラムから、インデックスによって [eventxfmod] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowEvent** <br/> |
| セル インデックス:  <br/> |**visEvtCellXFMod** <br/> |
   

