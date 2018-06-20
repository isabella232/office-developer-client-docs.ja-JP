---
title: '[DocLockDuplicatePage] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 97bca23a7dc9150f66eb0c87834fca72c215448b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805247"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>[DocLockDuplicatePage] セル ([ドキュメントのプロパティ] セクション)

ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。
  
|||
|:-----|:-----|
|TRUE  <br/> |**複製**のページのショートカット メニューと**Page.Duplicate**オートメーション メソッドの両方が無効です。  <br/> |
|FALSE  <br/> |このページは複製できます。  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **DocLockDuplicatePage** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | DocLockDuplicatePage  <br/> |
   
プログラムから、インデックスによって [ **DocLockDuplicatePage** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocLockDuplicatePage** <br/> |
   

