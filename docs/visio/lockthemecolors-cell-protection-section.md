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
ms.openlocfilehash: 2ca8af2c7a41259af73a111af331ce1031e5f46c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19805775"
---
# <a name="lockthemecolors-cell-protection-section"></a>[LockThemeColors] セル ([保護] セクション)

図形には、テーマの色のアプリケーションを防止します。 
  
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
   

