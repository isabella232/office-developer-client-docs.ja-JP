---
title: '[LockThemeFonts] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1ce8b52c-b6c1-4764-b4ec-00c7efb8929d
description: 新しいテーマを適用することで、[Theme Properties] 行の [FontIndex] セルが変更されないようにします。ユーザーが手動でシェイプシートのこの値を編集することは防げません。
ms.openlocfilehash: b90ffe4c5555df017bb0506a78351514c954ec39
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805799"
---
# <a name="lockthemefonts-cell-protection-section"></a>[LockThemeFonts] セル ([保護] セクション)

新しいテーマを適用することで、[**Theme Properties**] 行の [**FontIndex**] セルが変更されないようにします。ユーザーが手動でシェイプシートのこの値を編集することは防げません。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |[**FontIndex**] セルは、直接シェイプシートで変更しない限り、現在の値を変更できません。  <br/> |
|FALSE  <br/> |[**FontIndex**] セルは、テーマが変更された場合に現在の値を変更できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式によって、**Cell** エレメントの **N** 属性の値から、または **CellsU** プロパティを使用したプログラムから、名前によって [**LockThemeFonts**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockThemeFonts  <br/> |
   
プログラムから、インデックスによって [**LockThemeFonts**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockThemeFonts** <br/> |
   

