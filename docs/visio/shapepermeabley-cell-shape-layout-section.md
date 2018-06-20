---
title: '[ShapePermeableY] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
localization_priority: Normal
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。
ms.openlocfilehash: 4a7a389ec1d753b8582b7ff0b921a615e582b1ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806392"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>[ShapePermeableY] セル ([Shape Layout] セクション)

コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |コネクタの接続経路は、配置可能な図形上を垂直方向に通過します。  <br/> |
|FALSE  <br/> |コネクタの接続経路は、配置可能な図形上を垂直方向に通過できません。  <br/> |
   
## <a name="remarks"></a>注釈

**動作**] ダイアログ ボックスの [**配置**] タブで、このセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、[**配置**] タブをクリックして). 
  
Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ShapePermeableY] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapePermeableY  <br/> |
   
プログラムから、インデックスによって [ShapePermeableY] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPermY** <br/> |
   

