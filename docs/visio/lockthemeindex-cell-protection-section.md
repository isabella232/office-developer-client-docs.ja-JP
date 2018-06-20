---
title: '[LockThemeIndex] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: 新しいテーマを適用するか、新しいコネクタの設定を選択することによって変更されているテーマのプロパティの行のセルを ThemeIndex できないようにします。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805781"
---
# <a name="lockthemeindex-cell-protection-section"></a>[LockThemeIndex] セル ([保護] セクション)

新しいテーマを適用するか、新しいコネクタの設定を選択することによって変更されている**テーマのプロパティ**の行のセルを**ThemeIndex**できないようにします。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |シェイプ シートで直接変更しない限り、現在の値から**ThemeIndex**のセルを変更できません。  <br/> |
|FALSE  <br/> |テーマが変更されると、現在の値から**ThemeIndex**のセルを変更できます。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockThemeIndex** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockThemeIndex  <br/> |
   
プログラムから、インデックスによって [ **LockThemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockThemeIndex** <br/> |
   

