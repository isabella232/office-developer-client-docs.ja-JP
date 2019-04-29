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
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407761"
---
# <a name="lockbegin-cell-protection-section"></a>[LockBegin] セル ([Protection] セクション)

1-D 図形の始点 ([BeginX]、[BeginY]) を特定の位置にロックします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 始点をロックします。  <br/> |
| FALSE  <br/> | 始点をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockBegin] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [lockbegin]  <br/> |
   
プログラムから、インデックスによって [LockBegin] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockBegin** <br/> |
   

