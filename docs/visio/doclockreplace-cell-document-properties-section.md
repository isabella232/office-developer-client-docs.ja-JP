---
title: '[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 74eae5e5-80ab-4e10-b292-e58a6d7607d2
description: 置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。
ms.openlocfilehash: 41552ddad4e48680960c45869ded5cf4f80d760f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805271"
---
# <a name="doclockreplace-cell-document-properties-section"></a>[DocLockReplace] セル ([ドキュメントのプロパティ] セクション)

置換する図形の UI をこのドキュメントでは無効にするかどうかを決定します。 
  
|||
|:-----|:-----|
|TRUE  <br/> |**図形の置換**] ボタンが淡色表示 UI にします。  <br/> |
|FALSE  <br/> |**図形の置換**ボタンは、UI でアクティブです。 ユーザーは、この文書で、図形の置換機能を使用できます。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **DocLockReplace** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | DocLocReplace  <br/> |
   
プログラムから、インデックスによって [ **DocLocReplace** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowDoc** <br/> |
| セル インデックス:  <br/> |* * visDocLockReplace * * <br/> |
   

