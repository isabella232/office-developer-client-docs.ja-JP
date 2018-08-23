---
title: '[Comment] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60033
localization_priority: Normal
ms.assetid: b367841a-f31c-4b55-4491-2abab5811dbe
description: コメント内に表示されるテキストが含まれます。
ms.openlocfilehash: 443a229058a9ca910ba5b38b093706c9c2e3e95b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805028"
---
# <a name="comment-cell-annotation-section"></a>[Comment] セル ([注釈] セクション)

コメント内に表示されるテキストが含まれます。
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開くときにのみ、または .vsd ファイルの形式で .vsdx ファイルを保存するときにコメントを追跡するために使用されます。 Visio 2013 で .vsdx のドキュメント内のコメントを追跡するためには使用されません。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation.Comment [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visAnnotationComment** <br/> |
   

