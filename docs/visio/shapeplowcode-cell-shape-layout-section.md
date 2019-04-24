---
title: '[ShapePlowCode] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm900
localization_priority: Normal
ms.assetid: acf07fd7-6aa6-1a92-9b7a-bd6fea8a7cb2
description: 図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。
ms.openlocfilehash: 6e155103f7bfc70a78826297f441fc9ce78942ad
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325607"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>[ShapePlowCode] セル ([Shape Layout] セクション)

図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |ページの指定に従って移動します。  <br/> |**vissloん wdefault** <br/> |
|1-d  <br/> |どの図形も移動しません。  <br/> |**vissloの wnever** <br/> |
|pbm-2  <br/> |すべての図形が移動します。  <br/> |**visslo/always** <br/> |
   
## <a name="remarks"></a>解説

このセルの値は、[**基本動作**] ダイアログボックスの [**配置**] タブで、特定の図形に対して設定することもできます (図形が選択されている状態で、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] グループで、[**基本動作**] をクリックし、次にクリックします)。[**配置**] タブ)。 
  
図面ページ上の*すべて*の図形に対してこの動作を設定するには、[ページレイアウト] セクションの [コード] セルを使用します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlowCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[shapeplowcode]  <br/> |
   
プログラムから、インデックスによって [ShapePlowCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**vissloの wコード** <br/> |
   

