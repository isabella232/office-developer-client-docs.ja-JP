---
title: '[Date] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
ms.localizationpriority: medium
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: コメントを最後に編集した日付と時刻が含まれます。
ms.openlocfilehash: e899fe5b74f45a41a38f48710d5da297a50d5915
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612884"
---
# <a name="date-cell-annotation-section"></a>[Date] セル ([Annotation] セクション)

コメントを最後に編集した日付と時刻が含まれます。 
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開く場合、または .vsd ファイル形式で .vsdx ファイルを保存する場合にのみ、コメントを追跡するために使用されます。 2013 年の .vsdx ドキュメントのコメントを追跡Visioされません。 
  
## <a name="remarks"></a>注釈

ユーザー インターフェイスのコメント ボックスには、日付のみ表示されます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Date] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation.Date[  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Date] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visAnnotationDate** <br/> |
   

