---
title: '[X] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1028735
ms.localizationpriority: medium
ms.assetid: f9db8623-9fcf-7037-2d11-d509f463025d
description: ページ座標のコメント マーカーの x 座標。
ms.openlocfilehash: 931ea0ea6a1397dc02d91a93a76cc702e748fbe9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622607"
---
# <a name="x-cell-annotation-section"></a>[X] セル ([Annotation] セクション)

ページ  *座標*  のコメント マーカーの x 座標。 
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開く場合、または .vsd ファイル形式で .vsdx ファイルを保存する場合にのみ、コメントを追跡するために使用されます。 2013 年の .vsdx ドキュメントのコメントを追跡Visioされません。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation.X[  *i*  ]  *ここで、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visAnnotationX** <br/> |
   

