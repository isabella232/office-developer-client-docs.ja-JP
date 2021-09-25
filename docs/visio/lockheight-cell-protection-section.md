---
title: '[LockHeight] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
ms.localizationpriority: medium
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: 図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。
ms.openlocfilehash: fbc4ef93c7d3df306fe506aa09eed125743912d8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582555"
---
# <a name="lockheight-cell-protection-section"></a>[LockHeight] セル ([Protection] セクション)

図形の高さをロックします。ロックすると、図形のサイズを変更しても高さは変更されません。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 高さをロックします。  <br/> |
| FALSE  <br/> | 高さをロックしません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockHeight] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | LockHeight  <br/> |
   
プログラムから、インデックスによって [LockHeight] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLock** <br/> |
| セル インデックス:  <br/> |**visLockHeight** <br/> |
   

