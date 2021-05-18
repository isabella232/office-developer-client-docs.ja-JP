---
title: '[DirX / A] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251721
localization_priority: Normal
ms.assetid: 00d87b92-0da7-37d6-e7b5-23f350db0a9b
description: 一致する接続ポイントの必要な配置ベクトルの x -component を決定します。 [DirX / A] セルは、動的コネクタに付いている足の向きを揃える場合にも使用されます。 このセルでは浮動小数点値が使用されます。
ms.openlocfilehash: cb86ef1064537911ffd00a66f5c0b7942459f85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422398"
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
  

