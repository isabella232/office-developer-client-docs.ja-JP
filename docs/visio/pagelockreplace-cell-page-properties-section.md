---
title: '[PageLockReplace] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 59c36555-42af-4729-aea7-0332d1da6e3b
description: このページで [図形の置換] ボタンを無効にするかどうかを示します。
ms.openlocfilehash: c0495d47a81ed7a23e758c531f7d754291c47852
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433102"
---
# <a name="pagelockreplace-cell-page-properties-section"></a>[PageLockReplace] セル ([ページのプロパティ] セクション)

このページで [**図形の置換**] ボタンを無効にするかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |このページがアクティブなとき、[**図形の変更**] ボタンは灰色表示されます。  <br/> |
|FALSE  <br/> |このページによって [**図形の変更**] ボタンが無効になることはありません。**DocumentSheet** の **DocLockReplace** が **TRUE** に設定されている場合、または選択した図形の [**LockReplace**] セルが **TRUE** に設定されている場合は、このボタンが引き続き灰色表示される可能性があります。<br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**PageLockReplace**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PageLockReplace  <br/> |
   
プログラムから、インデックスによって [**PageLockReplace**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageLockReplace** <br/> |
   

