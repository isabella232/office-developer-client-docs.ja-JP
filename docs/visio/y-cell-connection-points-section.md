---
title: '[Y] セル ([Connection Points] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_SDR.chm1175
localization_priority: Normal
ms.assetid: 3af6c949-d6a0-9560-54d7-b01a2ad99960
description: 接続ポイントの y 座標をローカル座標で表します。
ms.openlocfilehash: b408dc3c07e7bd28c0530b09f649453b4f08c770
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360131"
---
# <a name="y-cell-connection-points-section"></a>[Y] セル ([Connection Points] セクション)

接続ポイントの*y*座標をローカル座標で表します。 
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Y] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 接続 Y *i* = <1> ** 、2、3...  <br/> |
   
プログラムから、インデックスによって [Y] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**持つ vissectionconnectionpts** <br/> |
| 行インデックス:  <br/> |**visRowConnectionPts** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visY** <br/> |
   

