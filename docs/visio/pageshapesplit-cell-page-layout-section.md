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
ms.openlocfilehash: 7f1df0158cde6853c5518597c853cb56151eefbc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805976"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>[PageShapeSplit] セル ([ページ レイアウト] セクション)

ページの図形が自動的に分割されるかどうかを示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |図形は自動的に分割されません。  <br/> |**visPLOSplitNone** <br/> |
|1  <br/> |図形は自動的に分割されます (既定値)。  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>注釈

図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。図形に関する既定の設定は、図面の種類によって異なります。 
  
アプリケーション レベルで分割を無効にするを有効または、 **Visio のオプション**] ダイアログ ボックスの [**詳細設定**] タブに**コネクタ分割を有効にする**設定を使用して、( **Office**ボタンをクリックし、 **Visio**の [**オプション**] をクリックしてタブをクリックし、[**詳細設定**] をクリック) します。 
  
図形レベルで分割を無効にするを有効またはは、[shapesplit] および [ShapeSplittable] セルを参照してください。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PageShapeSplit] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |PageShapeSplit  <br/> |
   
プログラムから、インデックスによって [PageShapeSplit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOSplit** <br/> |
   

