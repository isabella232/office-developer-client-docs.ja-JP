---
title: '[LockReplace] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b3880511-dd27-4dc2-9e50-a49084ef8195
description: 図形を置換操作に使用できるかどうか (ターゲット図形または置換後の図形のいずれかとして) を示します。
ms.openlocfilehash: 6f3e41d6a6c5b28c55e21961de63d0cc20eeb129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805761"
---
# <a name="lockreplace-cell-protection-section"></a>[LockReplace] セル ([保護] セクション)

図形を置換操作に使用できるかどうか (ターゲット図形または置換後の図形のいずれかとして) を示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図形は置換できません。または、置換後の図形として使用できません。  <br/> キャンバス上の図形、図形が選択されている場合に、[**図形の変更**] ボタンが無効です。  <br/> ステンシル上の図形、図形は表示されません置換後の図形と**図形の変更**] ボタンがクリックされたとき。  <br/> |
|FALSE  <br/> |図形は置換できます。または置換後の図形として使用できます。  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockReplace** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockReplace  <br/> |
   
プログラムから、インデックスによって [ **LockReplace** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockReplace** <br/> |
   

