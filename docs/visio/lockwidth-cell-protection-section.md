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
ms.openlocfilehash: abdcc0d5285e98e5856524925a41c4f72ee7f6ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805785"
---
# <a name="lockwidth-cell-protection-section"></a>[LockWidth] セル ([Protection] セクション)

図形の幅をロックします。ロックすると、図形のサイズを変更しても幅は変更されません。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 幅をロックします。  <br/> |
| FALSE  <br/> | 幅をロックしません。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [lockwidth] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [Lockwidth]  <br/> |
   
プログラムから、インデックスによって [lockwidth] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockWidth** <br/> |
   

