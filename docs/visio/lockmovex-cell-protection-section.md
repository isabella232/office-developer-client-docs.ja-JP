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
ms.openlocfilehash: 981f4f417e48f70d0693e30683c4351d0e53a758
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805777"
---
# <a name="lockmovex-cell-protection-section"></a>[LockMoveX] セル ([Protection] セクション)

図形の水平位置をロックします。ロックすると、図形は水平方向に移動できなくなります。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 水平位置をロックします。  <br/> |
| FALSE  <br/> | 水平位置をロックしません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [lockmovex] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Lockmovex]  <br/> |
   
プログラムから、インデックスによって [lockmovex] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockMoveX** <br/> |
   

