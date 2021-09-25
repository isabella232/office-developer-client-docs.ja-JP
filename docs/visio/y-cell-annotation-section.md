---
title: '[Y] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
ms.localizationpriority: medium
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: ページ座標のコメント マーカーの y 座標。
ms.openlocfilehash: 669e395c751770dfe160abff6ee23e227989ce32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603103"
---
# <a name="y-cell-annotation-section"></a>[Y] セル ([Annotation] セクション)

ページ  *座標の*  コメント マーカーの y 座標。 
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開く場合、または .vsd ファイル形式で .vsdx ファイルを保存する場合にのみ、コメントを追跡するために使用されます。 2013 年の .vsdx ドキュメントのコメントを追跡Visioされません。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation.Y [  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visAnnotationY** <br/> |
   

