---
title: '[LockGroup] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251227
localization_priority: Normal
ms.assetid: 04b0fa5b-1680-cfe2-6aaf-0502ad196027
description: グループをロックして、グループを解除できないようにします。
ms.openlocfilehash: 4d09d514a3fff8ada40c67eb9cd9537539a1039a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805773"
---
# <a name="lockgroup-cell-protection-section"></a>[LockGroup] セル ([保護] セクション)

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
|セル名:  <br/> |[Lockgroup]  <br/> |
   
プログラムから、インデックスによって [LockGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockGroup** <br/> |
   

