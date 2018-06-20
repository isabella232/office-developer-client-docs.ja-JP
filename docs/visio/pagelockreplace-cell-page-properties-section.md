---
title: '[PageLockReplace] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: このページの図形の置換] ボタンを無効にする必要があるかどうかを示します。
ms.openlocfilehash: b3956b3e2f2fcd5c4f82089e08a6e32200374778
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805964"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>[PageLockReplace] セル ([ページのプロパティ] セクション)

このページの**図形の置換**] ボタンを無効にする必要があるかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |このページがアクティブなときに、[**図形の変更**] ボタンは淡色表示されます。  <br/> |
|FALSE  <br/> |このページで、[**図形の変更**] ボタンが無効になっていません。 ボタンがまだ灰色場合: **DocumentSheet**の**DocLockReplace**になっている**場合は TRUE**です。選択した図形の**LockReplace**セルを**TRUE**に設定します。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **PageLockReplace** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PageLockReplace  <br/> |
   
プログラムから、インデックスによって [ **PageLockReplace** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageLockReplace** <br/> |
   

