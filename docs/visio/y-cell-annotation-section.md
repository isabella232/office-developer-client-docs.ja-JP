---
title: '[Y] セル ([Annotation] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60095
localization_priority: Normal
ms.assetid: 527a4615-2013-a4b4-81cd-7f5d71c1803c
description: ページ座標内のコメントマーカーの y 座標です。
ms.openlocfilehash: 48a37c261078cd1000331920b33549cee2c1da03
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360124"
---
# <a name="y-cell-annotation-section"></a>[Y] セル ([Annotation] セクション)

ページ座標内のコメントマーカーの*y*座標です。 
  
> [!NOTE]
> このセルは、Microsoft Visio 2013 で .vsd ファイルを開くとき、または .vsd ファイル形式で .vsdx ファイルを保存するときにのみ、コメントの追跡に使用されます。 これは、Visio 2013 の .vsdx ドキュメントでコメントを追跡するためには使用されません。 
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Annotation. Y [ *i* ] = ** <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionAnnotation** <br/> |
| 行インデックス:  <br/> |**visRowAnnotation** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visAnnotationY** <br/> |
   

