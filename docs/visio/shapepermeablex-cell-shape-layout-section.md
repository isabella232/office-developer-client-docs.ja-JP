---
title: '[ShapePermeableX] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm890
localization_priority: Normal
ms.assetid: 7e27b36c-4fd1-34e0-c168-f49eb5757b0e
description: コネクタの接続経路が、配置可能な図形上を水平方向に通過するかどうかを指定します。
ms.openlocfilehash: 1e0fe614b9401ea453b9c650ef9af3b4105b3805
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/15/2018
ms.locfileid: "19806401"
---
# <a name="shapepermeablex-cell-shape-layout-section"></a>[ShapePermeableX] セル ([図形レイアウト] セクション)

コネクタの接続経路が、配置可能な図形上を水平方向に通過するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |コネクタの接続経路は、配置可能な図形上を水平方向に通過します。  <br/> |
|FALSE  <br/> |コネクタの接続経路は、配置可能な図形上を水平方向に通過できません。  <br/> |
   
## <a name="remarks"></a>注釈

**動作**] ダイアログ ボックスの [**配置**] タブで、このセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、[**配置**] タブをクリックして). 
  
Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePermeableX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapePermeableX  <br/> |
   
プログラムから、インデックスによって [ShapePermeableX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPermX** <br/> |
   

