---
title: '[LockDelete] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
ms.localizationpriority: medium
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: 図形をロックして、削除できないようにします。
ms.openlocfilehash: dc746ae96dc5f8d359b1f7500b59fdbe7d7d86f8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554468"
---
# <a name="lockdelete-cell-protection-section"></a>[LockDelete] セル ([Protection] セクション)

図形をロックして、削除できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形は削除できません。  <br/> |
| FALSE  <br/> | 図形は削除できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockDelete] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockDelete  <br/> |
   
プログラムから、インデックスによって [LockDelete] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockDelete** <br/> |
   

