---
title: '[NoSnap] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm740
ms.localizationpriority: medium
ms.assetid: 0e6c8621-868c-9eac-926b-3049f18023b0
description: 他の図形がパスにスナップされるかどうかを指定します。
ms.openlocfilehash: ffb32cf8c0506eb8b4064f455258a7153bc123df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623321"
---
# <a name="nosnap-cell-geometry-section"></a>[NoSnap] セル ([Geometry] セクション)

他の図形がパスにスナップされるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 他の図形はこのパスにスナップできません。  <br/> |
| FALSE  <br/> | 他の図形はこのパスにスナップできます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoSnap] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Geometry  *i*  .NoSnap  *where i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [NoSnap] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...  <br/> |
| 行インデックス :  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoSnap** <br/> |
   

