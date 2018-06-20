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
ms.openlocfilehash: 00229dcabf45d2a3435039ffe05fd7eb4de75808
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805751"
---
# <a name="lockdelete-cell-protection-section"></a>[LockDelete] セル ([Protection] セクション)

図形をロックして、削除できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形は削除できません。  <br/> |
| FALSE  <br/> | 図形は削除できます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって LockDelete] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockDelete  <br/> |
   
プログラムから、インデックスによって [LockDelete] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockDelete** <br/> |
   

