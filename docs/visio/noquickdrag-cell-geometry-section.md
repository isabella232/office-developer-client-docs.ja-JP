---
title: '[NoQuickDrag] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80004
localization_priority: Normal
ms.assetid: 8491f459-9de2-8e75-5532-7d3bd0986734
description: ユーザーが [Geometry] セクションで定義された塗りつぶされた領域をクリックしたときに、図形を選択またはドラッグできるかどうかを指定します。
ms.openlocfilehash: d60268685d93ae88abb2840f62b093db1e688c2f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417722"
---
# <a name="noquickdrag-cell-geometry-section"></a>[NoQuickDrag] セル ([Geometry] セクション)

ユーザーが [Geometry] セクションで定義された塗りつぶされた領域をクリックしたときに、図形を選択またはドラッグできるかどうかを指定します。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoQuickDrag] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ジオメトリ*i*noquickdrag、where * i *-<1>、2、3...  <br/> |
   
プログラムから、インデックスによって [NoQuickDrag] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0、1、2...  <br/> |
|行インデックス :  <br/> |**visRowComponent** <br/> |
|セル インデックス:  <br/> |**visCompNoQuickDrag** <br/> |
   

