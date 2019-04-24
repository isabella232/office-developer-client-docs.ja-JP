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
ms.openlocfilehash: e0d1bb8a65b8087136e57bb46ad9f5363da30030
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359614"
---
# <a name="lockformat-cell-protection-section"></a>[LockFormat] セル ([Protection] セクション)

図形の書式設定をロックして、変更できないようにします。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 書式を変更できません。  <br/> |
| FALSE  <br/> | 書式を変更できます。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockFormat] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [lockformat]  <br/> |
   
プログラムから、インデックスによって [LockFormat] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockFormat** <br/> |
   

