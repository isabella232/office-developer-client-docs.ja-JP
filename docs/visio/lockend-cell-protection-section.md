---
title: '[LockEnd] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
ms.localizationpriority: medium
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: 1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。
ms.openlocfilehash: 35831023adb58b75be973bd6e54c5985eae01c0c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603614"
---
# <a name="lockend-cell-protection-section"></a>[LockEnd] セル ([Protection] セクション)

1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 終点をロックします。  <br/> |
| FALSE  <br/> | 終点をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockEnd] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockEnd  <br/> |
   
プログラムから、インデックスによって [LockEnd] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockEnd** <br/> |
   

