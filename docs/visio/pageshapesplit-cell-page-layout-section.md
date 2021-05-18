---
title: '[PageShapeSplit] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: ページの図形が自動的に分割されるかどうかを示します。
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422020"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>[PageShapeSplit] セル ([Page Layout] セクション)

ページの図形が自動的に分割されるかどうかを示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |図形の自動分割は許可しない。  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |自動図形分割を許可する (既定)。  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>注釈

図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。 既定では、分割はアプリケーションレベルとページ レベルで有効になっています。 図形の既定の設定は、図面の種類によって異なります。 
  
アプリケーション レベルで分割を有効または無効にするには、[Visioオプション] ダイアログボックスの [詳細設定] タブの [コネクタ分割を有効にする] 設定を使用します **(Office** ボタンをクリックし、[Visio]タブの [オプション] をクリックし、[詳細設定] をクリックします)。  
  
図形レベルでの分割を有効または無効にするには、ShapeSplit セルと ShapeSplittable セルを参照してください。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageShapeSplit] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PageShapeSplit  <br/> |
   
プログラムからインデックスによって PageShapeSplit セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOSplit** <br/> |
   

