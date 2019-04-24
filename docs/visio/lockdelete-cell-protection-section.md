---
title: '[LockDelete] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251219
localization_priority: Normal
ms.assetid: 596c62b7-8d42-1854-d709-592db09a6a84
description: 図形をロックして、削除できないようにします。
ms.openlocfilehash: 0819969c9ba17a52de19341b359b33ceae5b44d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359620"
---
# <a name="lockdelete-cell-protection-section"></a>[LockDelete] セル ([Protection] セクション)

図形をロックして、削除できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形は削除できません。  <br/> |
| FALSE  <br/> | 図形は削除できます。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockDelete] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [lockdelete]  <br/> |
   
プログラムから、インデックスによって [LockDelete] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockDelete** <br/> |
   

