---
title: '[X] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251746
localization_priority: Normal
ms.assetid: 11c69600-4e1f-4c52-ff35-b6a7cc6c734c
description: 接続ポイントの x 座標をローカル座標で表します。
ms.openlocfilehash: 496e5af6ea5b7ba99730b23dcbb510db6af9b23b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339880"
---
# <a name="x-cell-connection-points-section"></a>[X] セル ([Connection Points] セクション)

接続ポイントの*x*座標をローカル座標で表します。 
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [X] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 接続 X *i* = <1> ** 、2、3...  <br/> |
   
プログラムから、インデックスによって [X] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**持つ vissectionconnectionpts** <br/> |
| 行インデックス:  <br/> |**visRowConnectionPts** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visx** <br/> |
   

