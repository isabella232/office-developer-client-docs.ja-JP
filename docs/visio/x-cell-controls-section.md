---
title: '[X] セル ([Controls] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251281
ms.localizationpriority: medium
ms.assetid: b7aea554-f491-6a9a-4d07-feeab739a9df
description: ローカル座標での図形のコントロール ハンドルの位置を示す x 座標を表します。
ms.openlocfilehash: 948b27415d22f4beb2d4c6d0c3a14e53252920f2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582522"
---
# <a name="x-cell-controls-section"></a>[X] セル ([Controls] セクション)

ローカル座標での  *図形*  のコントロール ハンドルの位置を示す x 座標を表します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | コントロール。  *name*  .X where Controls.  *name*  は、コントロール行の名前です。  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionControls** <br/> |
| 行インデックス:  <br/> |**visRowControl**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visCtlX** <br/> |
   

