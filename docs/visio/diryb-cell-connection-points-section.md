---
title: '[DirY / B] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm240
ms.localizationpriority: medium
ms.assetid: d951c57d-2c22-0289-35af-44e3c2877b2c
description: 一致する接続ポイントの必要な配置ベクトルの y -component を決定します。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数値が使用されます。
ms.openlocfilehash: af2801f32533d5b82b9f3133dbc700444f04ff43
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59574420"
---
# <a name="diry--b-cell-connection-points-section"></a>[DirY / B] セル ([Connection Points] セクション)

一致する  *接続ポイントの*  必要な配置ベクトルの y -component を決定します。 動的コネクタに付いている脚の向きを揃える場合にも使用されます。 このセルでは浮動小数点値が使用されます。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DirY / B] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |Connections.DirY[ i ]*ここで**、i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [DirY / B] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionConnectionPts** <br/> |
|行インデックス:  <br/> |**visRowConnectionPts**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visCnnctDirY** (拡張されていない行)           **visCnnctB** (拡張行)  <br/> |
   
拡張されていない行および拡張された行の詳細については、[Connection Points] 行を参照してください。
  

