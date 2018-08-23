---
title: '[LockBegin] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: 1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805736"
---
# <a name="lockbegin-cell-protection-section"></a>[LockBegin] セル ([保護] セクション)

1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 始点をロックします。  <br/> |
| FALSE  <br/> | 始点をロックしません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockBegin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Lockbegin]  <br/> |
   
プログラムから、インデックスによって [LockBegin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockBegin** <br/> |
   

