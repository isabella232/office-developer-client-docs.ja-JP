---
title: '[NoSnap] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
localization_priority: Normal
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: 他の図形がパスにスナップされるかどうかを指定します。
ms.openlocfilehash: 111f3773cb1df9033ed5a7b0b146d40ce6b26df0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805933"
---
# <a name="nosnap-cell-geometry-section"></a>[NoSnap] セル ([Geometry] セクション)

他の図形がパスにスナップされるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 他の図形はこのパスにスナップできません。  <br/> |
| FALSE  <br/> | 他の図形はこのパスにスナップできます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [nosnap] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。[Nosnap]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [nosnap] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoSnap** <br/> |
   

