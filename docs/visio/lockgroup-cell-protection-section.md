---
title: '[LockGroup] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
ms.localizationpriority: medium
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: グループをロックして、グループを解除できないようにします。
ms.openlocfilehash: cdb251fb66e522d2b2200f324b63410d9e83be1c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612499"
---
# <a name="lockgroup-cell-protection-section"></a>[LockGroup] セル ([Protection] セクション)

グループをロックして、グループを解除できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グループを解除できません。  <br/> |
|FALSE  <br/> |グループを解除できます。  <br/> |
   
## <a name="remarks"></a>注釈

[LockGroupCell] 値を TRUE に設定すると、グループのメンバーである図形が削除されるのを防ぐこともできます。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockGroup] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockGroup  <br/> |
   
プログラムから、インデックスによって [LockGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockGroup** <br/> |
   

