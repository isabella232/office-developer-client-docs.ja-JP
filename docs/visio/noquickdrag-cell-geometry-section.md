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
description: 図形の選択またはユーザーは、[Geometry] セクションで定義されている塗りつぶしの領域をクリックしたときにドラッグするかどうかを決定します。
ms.openlocfilehash: 7d4ffd876d8676af885b8f750fecf6f6d0deaa9b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805932"
---
# <a name="noquickdrag-cell-geometry-section"></a>[NoQuickDrag] セル ([Geometry] セクション)

図形の選択またはユーザーは、[Geometry] セクションで定義されている塗りつぶしの領域をクリックしたときにドラッグするかどうかを決定します。
  
## <a name="remarks"></a>備考

参照を取得する NoQuickDrag のセルに名前を別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ジオメトリの*i*です。NoQuickDrag、* i * - < 1 > 2、3.  <br/> |
   
プログラムから、インデックスによって [NoQuickDrag] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|行インデックス:  <br/> |**visRowComponent** <br/> |
|セル インデックス:  <br/> |**visCompNoQuickDrag** <br/> |
   

