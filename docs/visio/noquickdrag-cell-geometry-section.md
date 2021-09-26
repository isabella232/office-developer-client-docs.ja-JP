---
title: '[NoQuickDrag] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
ms.localizationpriority: medium
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: ユーザーが [Geometry] セクションで定義された塗りつぶされた領域をクリックすると、図形を選択またはドラッグできるかどうかを指定します。
ms.openlocfilehash: 052080f2334eb776e8a50d608724a6faa445d2ab
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627871"
---
# <a name="noquickdrag-cell-geometry-section"></a>[NoQuickDrag] セル ([Geometry] セクション)

ユーザーが [Geometry] セクションで定義された塗りつぶされた領域をクリックすると、図形を選択またはドラッグできるかどうかを指定します。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoQuickDrag] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |Geometry  *i*  .NoQuickDrag、ここで * i * - <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [NoQuickDrag] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionFirstComponent**  +  *i* , *where i* = 0, 1, 2...  <br/> |
|行インデックス :  <br/> |**visRowComponent** <br/> |
|セル インデックス:  <br/> |**visCompNoQuickDrag** <br/> |
   

