---
title: '[X] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
ms.localizationpriority: medium
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: ローカル座標の接続点の x 座標を表します。
ms.openlocfilehash: 5703cd13e6679a97cfdd576e1972e806d3353a39
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549302"
---
# <a name="x-cell-connection-points-section"></a>[X] セル ([Connection Points] セクション)

ローカル座標の  *接続点*  の x 座標を表します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Connections.X  *i*            *は、i*  = <1>、2、3..です。  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
| 行インデックス:  <br/> |**visRowConnectionPts**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visX** <br/> |
   

