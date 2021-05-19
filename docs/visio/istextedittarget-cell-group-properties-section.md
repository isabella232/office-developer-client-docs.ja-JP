---
title: '[IsTextEditTarget] セル ([Group Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251627
localization_priority: Normal
ms.assetid: 355cef8b-9213-479a-af95-b591f4bc51ad
description: グループに対するテキストの割り当て方を指定します。
ms.openlocfilehash: 78a70dc0398745765bca12a1e768390b35fce8ce
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432647"
---
# <a name="istextedittarget-cell-group-properties-section"></a>[IsTextEditTarget] セル ([Group Properties] セクション)

グループに対するテキストの割り当て方を指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストはグループ図形に追加されます。  <br/> |
|FALSE  <br/> |テキストは、グループ内で積み重ねられた図形の中で、最前面にある図形に追加されます。  <br/> |
   
## <a name="remarks"></a>注釈

このセルの値は、グループを選択して、[[開発者用](run-in-developer-mode-display-the-developer-tab.md)] タブで [**基本動作**] をクリックし、[**グループのテキストを編集**] チェック ボックスをオンにして設定することもできます。 
  
Visio 2000 より前のバージョンで作成したグループの場合、既定値は FALSE です。Visio バージョン 2000 以降、既定値は TRUE になっています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [IsTextEditTarget] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |IsTextEditTarget  <br/> |
   
プログラムから、インデックスによって [IsTextEditTarget] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス :  <br/> |**visRowGroup** <br/> |
|セル インデックス:  <br/> |**visGroupIsTextEditTarget** <br/> |
   

