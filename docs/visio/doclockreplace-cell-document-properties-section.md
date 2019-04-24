---
title: '[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: 置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。
ms.openlocfilehash: cfec9b3c51a170c549fdd0d1b0b3597c030c410c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338606"
---
# <a name="doclockreplace-cell-document-properties-section"></a>[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)

置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。 
  
|||
|:-----|:-----|
|TRUE  <br/> |UI の [**図形の置換**] ボタンは灰色表示されます。  <br/> |
|FALSE  <br/> |UI の [**図形の置換**] ボタンはアクティブです。ユーザーはこのドキュメントで [図形の置換] 機能を使用できます。図形の置換<br/> |
   
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**DocLockReplace**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | doclocreplace  <br/> |
   
プログラムから、インデックスによって [**DocLocReplace**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |* * visDocLockReplace * * <br/> |
   

