---
title: '[LockWidth] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
ms.localizationpriority: medium
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: 図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。
ms.openlocfilehash: 5e3b05fb7cda925c5d1c4e2942c665d55190cc7d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582562"
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
| セル名:  <br/> | LockWidth  <br/> |
   
プログラムから、インデックスによって [LockWidth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockWidth** <br/> |
   

