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
ms.openlocfilehash: fd9dce2618c0b8c967b794b0beea8b772a231003
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415531"
---
# <a name="comment-cell-annotation-section"></a>[Comment] セル ([Annotation] セクション)

コメント内に表示されるテキストが含まれます。
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開くとき、または .vsd ファイル形式で .vsdx ファイルを保存するときにのみ、コメントの追跡に使用されます。 これは、Visio 2013 の .vsdx ドキュメントでコメントを追跡するためには使用されません。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Comment] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | コメント [ *i* ]: *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Comment] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visAnnotationComment** <br/> |
   

