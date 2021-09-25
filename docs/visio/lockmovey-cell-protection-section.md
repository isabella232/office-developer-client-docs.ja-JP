---
title: '[LockMoveY] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
ms.localizationpriority: medium
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: 図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。
ms.openlocfilehash: e3e8b2e95d966e94f9a211dc082ace722674f2d6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627976"
---
# <a name="lockmovey-cell-protection-section"></a>[LockMoveY] セル ([Protection] セクション)

図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 垂直位置をロックします。  <br/> |
| FALSE  <br/> | 垂直位置をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockMoveY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockMoveY  <br/> |
   
プログラムから、インデックスによって [LockMoveY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockMoveY** <br/> |
   

