---
title: '[Date] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60036
localization_priority: Normal
ms.assetid: f1f11803-614b-a40d-0a2d-131093e7609e
description: コメントを最後に編集した日付と時刻が含まれます。
ms.openlocfilehash: 4b6e7ea70302b10728d82f36ad0db39077af9523
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805181"
---
# <a name="date-cell-annotation-section"></a>[Date] セル ([Annotation] セクション)

コメントを最後に編集した日付と時刻が含まれます。 
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。 Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。 
  
## <a name="remarks"></a>備考

ユーザー インターフェイスのコメント ボックスには、日付のみ表示されます。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Date] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation.Date [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Date] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visAnnotationDate** <br/> |
   

