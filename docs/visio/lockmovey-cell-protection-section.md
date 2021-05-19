---
title: '[LockMoveY] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: 図形の垂直位置をロックします。ロックすると、図形は垂直方向に移動できなくなります。
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434047"
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
   

