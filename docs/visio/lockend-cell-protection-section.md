---
title: '[LockEnd] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm620
localization_priority: Normal
ms.assetid: e9742142-4d34-1ba9-480e-d1ecff4fc7cd
description: 1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。
ms.openlocfilehash: d29f07e5b4b77ed2fb8b104769a2fdca55abcc8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805754"
---
# <a name="lockend-cell-protection-section"></a>[LockEnd] セル ([Protection] セクション)

1-D 図形の終点 ([EndX]、[EndY]) を特定の位置にロックします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 終点をロックします。  <br/> |
| FALSE  <br/> | 終点をロックしません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [lockend] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Lockend]  <br/> |
   
プログラムから、インデックスによって [lockend] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockEnd** <br/> |
   

