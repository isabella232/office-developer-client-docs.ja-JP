---
title: '[Y] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
ms.localizationpriority: medium
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: ローカル座標の接続点の y 座標を表します。
ms.openlocfilehash: cceced17d52a847a5b1d2fb96e7995a1e543aaad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59553551"
---
# <a name="y-cell-connection-points-section"></a>[Y] セル ([Connection Points] セクション)

ローカル座標の  *接続点の y*  座標を表します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Connections.Y  *i*            i =  *<*  1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
| 行インデックス:  <br/> |**visRowConnectionPts**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visY** <br/> |
   

