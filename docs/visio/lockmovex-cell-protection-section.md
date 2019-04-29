---
title: '[LockMoveX] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: 図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435860"
---
# <a name="lockmovex-cell-protection-section"></a>[LockMoveX] セル ([Protection] セクション)

図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 水平位置をロックします。  <br/> |
| FALSE  <br/> | 水平位置をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockMoveX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [lockmovex]  <br/> |
   
プログラムから、インデックスによって [LockMoveX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockMoveX** <br/> |
   

