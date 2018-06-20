---
title: '[LockHeight] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: 図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805760"
---
# <a name="lockheight-cell-protection-section"></a>[LockHeight] セル ([Protection] セクション)

図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 高さをロックします。  <br/> |
| FALSE  <br/> | 高さをロックしません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockHeight] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockHeight  <br/> |
   
プログラムから、インデックスによって [LockHeight] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockHeight** <br/> |
   

