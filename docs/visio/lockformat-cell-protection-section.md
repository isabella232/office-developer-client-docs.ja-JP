---
title: '[LockFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm625
ms.localizationpriority: medium
ms.assetid: e9a640f4-0af0-317c-b77b-f32c651e87b4
description: 図形の書式設定をロックして、変更できないようにします。
ms.openlocfilehash: cbc0af1032a25a4939cbf16bb0586cf18a119cf6
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603628"
---
# <a name="lockformat-cell-protection-section"></a>[LockFormat] セル ([Protection] セクション)

図形の書式設定をロックして、変更できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 書式を変更できません。  <br/> |
| FALSE  <br/> | 書式を変更できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockFormat] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockFormat  <br/> |
   
プログラムから、インデックスによって [LockFormat] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockFormat** <br/> |
   

