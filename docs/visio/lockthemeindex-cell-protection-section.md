---
title: '[LockThemeIndex] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7b781727-267b-4589-ab40-cfc79bb96c2d
description: '[テーマのプロパティ] 行の [ThemeIndex] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。'
ms.openlocfilehash: 4bef3eb799c943ff89027e69ae8580c9c0e51243
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805781"
---
# <a name="lockthemeindex-cell-protection-section"></a>[LockThemeIndex] セル ([保護] セクション)

[**テーマのプロパティ**] 行の [**ThemeIndex**] セルが、新しいテーマの適用または新しいコネクタ スキーマの選択によって変更されないようにします。ユーザーがシェイプシートのこの値を手動で変更することは防げません。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |シェイプシートを直接変更しない限り、[**ThemeIndex**] セルの現在の値は変更できません。  <br/> |
|FALSE  <br/> |テーマが変更された場合、 [**ThemeIndex**] セルの現在の値を変更できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeIndex**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockThemeIndex  <br/> |
   
プログラムから、インデックスによって [**LockThemeIndex**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockThemeIndex** <br/> |
   

