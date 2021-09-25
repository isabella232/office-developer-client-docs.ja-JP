---
title: '[Comment] セル ([Miscellaneous] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm170
ms.localizationpriority: medium
ms.assetid: 6f52ed60-d58b-86e6-f7e2-2ef19d4afa75
description: 図形のコメント テキストを文字列形式で格納します。
ms.openlocfilehash: 6e243599d4f370e477f52868c980e37f461dc902
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603747"
---
# <a name="comment-cell-miscellaneous-section"></a>[Comment] セル ([Miscellaneous] セクション)

図形のコメント テキストを文字列形式で格納します。
  
## <a name="remarks"></a>注釈

コメントは、[**校閲**] タブの [**新しいコメント**] をクリックして挿入することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |コメント  <br/> |
   
プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowMisc** <br/> |
|セル インデックス:  <br/> |**visComment** <br/> |
   

