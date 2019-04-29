---
title: '[LockWidth] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: 図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439808"
---
# <a name="lockwidth-cell-protection-section"></a>[LockWidth] セル ([Protection] セクション)

図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 幅をロックします。  <br/> |
| FALSE  <br/> | 幅をロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockWidth] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [lockwidth]  <br/> |
   
プログラムから、インデックスによって [LockWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockWidth** <br/> |
   

