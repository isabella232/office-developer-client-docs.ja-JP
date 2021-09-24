---
title: '[ShapeSplit] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60080
ms.localizationpriority: medium
ms.assetid: 96b8c503-67b3-8623-d99b-0dad7b15c224
description: この図形が、分割可能な図形を分割できるかどうかを示します。
ms.openlocfilehash: da89333e8a190d2ad573b1d088480c5e0df6efd8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549610"
---
# <a name="shapesplit-cell-shape-layout-section"></a>[ShapeSplit] セル ([Shape Layout] セクション)

この図形が、分割可能な図形を分割できるかどうかを示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | この図形は他の図形を分割できません。  <br/> |**visSLOSplitNone** <br/> |
| 1  <br/> | この図形は他の図形を分割できます。  <br/> |**visSLOSplitAllow** <br/> |
   
## <a name="remarks"></a>注釈

他の図形を分割できる図形は、2 次元図形か 1 次元の配置可能な図形のどちらかである必要があります。 
  
図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。既定では、アプリケーション レベルとページ レベルで分割できます。図形レベルでは、図面の種類によって異なります。 
  
アプリケーション レベルで分割を有効または無効にするには **、[Visio** オプション] ダイアログボックスの [詳細設定] タブの [コネクタ分割を有効にする]設定を使用します ([ファイル] タブをクリックし、[オプション] をクリックし、[詳細設定] をクリック **します)。**  
  
ページで分割を有効または無効にするには、[PageShapeSplit] セルを使用します。 
  
1 次元図形を分割可能にするには、[ShapeSplittable] セルを使用します。
  
別の数式または CellsU プロパティを使用してプログラムから名前によって [ShapeSplit] セルへの参照を取得するには、次の値 **を使用** します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ShapeSplit  <br/> |
   
プログラムから、インデックスによって [ShapeSplit] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowShapeLayout** <br/> |
| セル インデックス:  <br/> |**visSLOSplit** <br/> |
   

