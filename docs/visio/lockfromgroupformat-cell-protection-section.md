---
title: '[LockFromGroupFormat] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: abd175af-ad4e-b84a-2687-2c9358653499
ms.openlocfilehash: ef4cd97298108f64f4fdc7fcd5d690bfeeb16bbc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554447"
---
# <a name="lockfromgroupformat-cell-protection-section"></a>[LockFromGroupFormat] セル ([Protection] セクション)

グループ図形に対する変更がサブ図形に伝達されるのをブロックし、ユーザーは選択したサブ図形を直接書式設定できます。 
  
[LockFromGroupFormat] セルの値は、[**保護**] ダイアログ ボックスにある [**グループ書式設定を適用不可にする**] チェック ボックスの設定に対応します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [LockFromGroupFormat] セルへの参照を取得するには、次の値を使用します。

 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockFromGroupFormat  <br/> |
   
プログラムから、インデックスによって [LockFromGroupFormat] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockFromGroupFormat** <br/> |
   
セルの既定値は 0 (False) となります。
  

