---
title: '[LockFromGroupFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: 3daeb4704a33ba836cf82c9ab3517c6ca6be8db7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359592"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>[LockFromGroupFormat] セル ([Protection] セクション)

グループ図形の書式設定の変更がサブ図形に反映されないようにしながら、選択したサブ図形の書式を直接設定できるようにします。 
  
[LockFromGroupFormat] セルの値は、[**保護**] ダイアログ ボックスにある [**グループ書式設定を適用不可にする**] チェック ボックスの設定に対応します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockFromGroupFormat] セルへの参照を取得するには、次の値を使用します。

 
  
|||
|:-----|:-----|
|セル名:  <br/> |[lockfromgroupformat]  <br/> |
   
プログラムから、インデックスによって [LockFromGroupFormat] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockFromGroupFormat** <br/> |
   
セルの既定値は 0 (False) となります。
  

