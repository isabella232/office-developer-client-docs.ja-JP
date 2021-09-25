---
title: '[BeginGroup] セル ([Actions] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60022
ms.localizationpriority: medium
ms.assetid: 1ae7f629-fb9f-1a11-1194-b381d6c9de5b
description: このアクションのメニューに区切り記号を挿入するかどうかを示します。
ms.openlocfilehash: 7f6ce3836cf71adcdb7135c390abc84834d57fad
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616027"
---
# <a name="begingroup-cell-actions-section"></a>[BeginGroup] セル ([Actions] セクション)

このアクションのメニューに区切り記号を挿入するかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |このアクションのメニューに区切り記号を挿入します。  <br/> |
|FALSE  <br/> |このアクションのメニューに区切り記号を挿入しません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginGroup] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |アクション。 *name*.BeginGroup where Actions. *name* には [Actions] 行の名前を指定  <br/> |
   
プログラムから、インデックスによって [BeginGroup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionAction** <br/> |
|行インデックス:  <br/> |**visRowAction**  +  *i* *=* 0, 1, 2...  <br/> |
|セル インデックス:  <br/> |**visActionBeginGroup** <br/> |
   

