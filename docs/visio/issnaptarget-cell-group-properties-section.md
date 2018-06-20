---
title: '[IsSnapTarget] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251626
localization_priority: Normal
ms.assetid: b58131f6-a566-d9ca-bad4-4f4b66e03aaf
description: グループにスナップするかグループ内の図形にスナップするかを指定します。
ms.openlocfilehash: 89536923617f80768d7c14658cb07c97595824ea
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805626"
---
# <a name="issnaptarget-cell-group-properties-section"></a>[IsSnapTarget] セル ([Group Properties] セクション)

グループにスナップするかグループ内の図形にスナップするかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |グループ内の図形へのスナップを有効にします。  <br/> |
|FALSE  <br/> |グループにのみスナップします。  <br/> |
   
## <a name="remarks"></a>注釈

[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブ**の動作**をクリックすると、グループを選択し、 **[メンバー図形にスナップ**] チェック ボックスをオンにしてこの値を設定することもできます。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[IsSnapTarget] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |IsSnapTarget  <br/> |
   
プログラムから、インデックスによって [IsSnapTarget] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupIsSnapTarget** <br/> |
   

