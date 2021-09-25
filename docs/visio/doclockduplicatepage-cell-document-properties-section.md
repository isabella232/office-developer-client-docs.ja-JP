---
title: '[DocLockDuplicatePage] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b08a6558-519f-44e0-aeff-9919544d515e
description: ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 264b55909a5eb48636601566d6392e62393f00d9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559921"
---
# <a name="doclockduplicatepage-cell-document-properties-section"></a>[DocLockDuplicatePage] セル ([ドキュメントのプロパティ] セクション)

ドキュメントのページを複製できるかどうかを、ブール演算型で決定します。
  
|||
|:-----|:-----|
|TRUE  <br/> |ページのショートカット メニューの  [**複製**] と、**Page.Duplicate** オートメーション メソッドはどちらも無効化されています。  <br/> |
|FALSE  <br/> |このページは複製できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**DocLockDuplicatePage**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | DocLockDuplicatePage  <br/> |
   
プログラムから、インデックスによって [**DocLockDuplicatePage**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |**visDocLockDuplicatePage** <br/> |
   

