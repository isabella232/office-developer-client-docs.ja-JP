---
title: '[Comment] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
ms.localizationpriority: medium
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: コメント内に表示されるテキストが含まれます。
ms.openlocfilehash: eb015489e9a396dc39141ad5b3beb68bbe88e2a5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628613"
---
# <a name="comment-cell-annotation-section"></a>[Comment] セル ([Annotation] セクション)

コメント内に表示されるテキストが含まれます。
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開く場合、または .vsd ファイル形式で .vsdx ファイルを保存する場合にのみ、コメントを追跡するために使用されます。 2013 年の .vsdx ドキュメントのコメントを追跡Visioされません。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation.Comment[  *i*  ]  *ここで、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visAnnotationComment** <br/> |
   

