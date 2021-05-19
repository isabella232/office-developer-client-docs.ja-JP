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
ms.openlocfilehash: c9f762f390dbea1e4ff2bd5bcf9566b8c67df11f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409756"
---
# <a name="lockselect-cell-protection-section"></a>[LockSelect] セル ([Protection] セクション)

図形の選択操作ができないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形を選択できません。  <br/> |
| FALSE  <br/> | 図形を選択できます。  <br/> |
   
## <a name="remarks"></a>注釈

[LockSelect] を有効にするには、[**図面の保護**] ダイアログ ボックスの [**図形**] チェック ボックスをオンにする必要があります。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockSelect] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockSelect  <br/> |
   
プログラムから、インデックスによって [LockSelect] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockSelect** <br/> |
   

