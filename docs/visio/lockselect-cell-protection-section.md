---
title: '[LockSelect] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm660
localization_priority: Normal
ms.assetid: c96b45a5-719e-8c4b-71b9-cb2224d83e21
description: 図形の選択操作ができないようにします。
ms.openlocfilehash: 082e993f7773640f59022c46458563d491197908
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805780"
---
# <a name="lockselect-cell-protection-section"></a>[LockSelect] セル ([Protection] セクション)

図形の選択操作ができないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を選択できません。  <br/> |
| FALSE  <br/> | 図形を選択できます。  <br/> |
   
## <a name="remarks"></a>備考

Lockselect] を有効にするために有効で、**文書の保護**] ダイアログ ボックスで、[**図形**] チェック ボックスを選択してください。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって lockselect] を有効] セルへの参照を取得するには、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Lockselect] を有効  <br/> |
   
プログラムから、インデックスによって [lockselect] を有効] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockSelect** <br/> |
   

