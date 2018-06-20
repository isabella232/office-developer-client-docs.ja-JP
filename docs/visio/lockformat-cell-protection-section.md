---
title: '[LockFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
localization_priority: Normal
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: 図形の書式設定をロックして、変更できないようにします。
ms.openlocfilehash: c3e4d5be848e91554406e709ce6872ae49b5f38d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805753"
---
# <a name="lockformat-cell-protection-section"></a>[LockFormat] セル ([Protection] セクション)

図形の書式設定をロックして、変更できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 書式を変更できません。  <br/> |
| FALSE  <br/> | 書式を変更できます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[LockFormat] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockFormat  <br/> |
   
プログラムから、インデックスによって [LockFormat] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockFormat** <br/> |
   

