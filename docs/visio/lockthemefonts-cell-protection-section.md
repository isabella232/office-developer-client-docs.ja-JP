---
title: '[LockThemeFonts] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: FontIndex、テーマのプロパティの行のセルが新しいテーマを適用することによって変更するを防ぎます。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805799"
---
# <a name="lockthemefonts-cell-protection-section"></a>[LockThemeFonts] セル ([保護] セクション)

**FontIndex** **テーマのプロパティ**の行のセルが新しいテーマを適用することによって変更するを防ぎます。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |シェイプ シートで直接変更しない限り、現在の値から**FontIndex**のセルを変更できません。  <br/> |
|FALSE  <br/> |テーマが変更されると、現在の値から**FontIndex**のセルを変更できます。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockThemeFonts** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockThemeFonts  <br/> |
   
プログラムから、インデックスによって [ **LockThemeFonts** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockThemeFonts** <br/> |
   

