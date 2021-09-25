---
title: '[DirX / A] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
ms.localizationpriority: medium
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: 一致する接続ポイントの必要な配置ベクトルの x -component を決定します。 [DirX / A] セルは、動的コネクタに付いている足の向きを揃える場合にも使用されます。 このセルでは浮動小数点値が使用されます。
ms.openlocfilehash: d287568ac43ebb1f80d1914c22d81c843c44c7fd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628473"
---
# <a name="dirx--a-cell-connection-points-section"></a>[DirX / A] セル ([Connection Points] セクション)

一致する  *接続ポイントの*  必要な配置ベクトルの x -component を決定します。 [DirX / A] セルは、動的コネクタに付いている足の向きを揃える場合にも使用されます。 このセルでは浮動小数点値が使用されます。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirX / A] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Connections.DirX[ i ]*ここで**、i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [DirX / A] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
| 行インデックス:  <br/> |**visRowConnectionPts**  +  *i* *=* 0、1、2  <br/> |
| セル インデックス:  <br/> |**visCnnctDirX** (拡張されていない行)           **visCnnctA** (拡張行)  <br/> |
   
拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。
  

