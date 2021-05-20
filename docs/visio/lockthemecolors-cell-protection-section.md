---
title: '[LockThemeColors] セル ([Protection] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm70001
localization_priority: Normal
ms.assetid: 22cedeb3-58b5-3932-9252-5c9dd3e163e3
ms.openlocfilehash: 81091ea33be2158435d240ba14f3c97e8f3fcc39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436847"
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
   

