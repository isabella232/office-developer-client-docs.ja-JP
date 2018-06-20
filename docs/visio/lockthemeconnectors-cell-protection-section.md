---
title: '[LockThemeConnectors] セル ([保護] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ae7ddd55-7bcc-4bb6-bab7-97806122f166
description: ConnectorsSchemeIndex、テーマのプロパティの行のセルが、新しいテーマを適用するか、新しいコネクタの設定を選択すると変更するを防ぎます。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。
ms.openlocfilehash: c74bcf554f0f14de47480397a96680469826d2c2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805778"
---
# <a name="lockthemeconnectors-cell-protection-section"></a>[LockThemeConnectors] セル ([保護] セクション)

**ConnectorsSchemeIndex** **テーマのプロパティ**の行のセルが、新しいテーマを適用するか、新しいコネクタの設定を選択すると変更するを防ぎます。 でも、ユーザーからシェイプ シート内でこの値を手動で編集します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |シェイプ シートで直接変更しない限り、現在の値から**ConnectorsSchemeIndex**のセルを変更できません。  <br/> |
|FALSE  <br/> |**ConnectorsSchemeIndex**セルは、ui の現在の値から変更できます。  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **LockThemeConnectors** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockThemeConnectors  <br/> |
   
プログラムから、インデックスによって [ **LockThemeConnectors** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockThemeConnectors** <br/> |
   

