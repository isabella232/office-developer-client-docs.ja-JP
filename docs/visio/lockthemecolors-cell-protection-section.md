---
title: '[LockThemeColors] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
ms.localizationpriority: medium
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: e4a96cab2939c17980a7f0daba6af65ddcac4045
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623377"
---
# <a name="lockthemecolors-cell-protection-section"></a>[LockThemeColors] セル ([Protection] セクション)

テーマの色が図形に適用されるのを防ぐ。 
  
[LockThemeColors] セルの値は、[**保護**] ダイアログ ボックスの [**テーマの色を適用不可にする**] チェックボックスの設定に対応します。 
  
別の数式または  **CellsU** プロパティを使用したプログラムから、名前によって [LockThemeColors] セルを参照するには、次の値を使用します。

 
  
|||
|:-----|:-----|
|セル名:  <br/> |LockThemeColors  <br/> |
   
プログラムから、インデックスによって [LockThemeColors] セルを参照するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowLock** <br/> |
|セル インデックス:  <br/> |**visLockThemeColors** <br/> |
   

