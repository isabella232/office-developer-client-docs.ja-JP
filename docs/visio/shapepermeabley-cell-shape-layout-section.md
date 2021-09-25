---
title: '[ShapePermeableY] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251666
ms.localizationpriority: medium
ms.assetid: 90701ecf-3d34-2eac-9ee9-7965e16c0f7c
description: コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。
ms.openlocfilehash: c4625eadf2d9729c08204eac6d6d12b9b7f69408
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573356"
---
# <a name="shapepermeabley-cell-shape-layout-section"></a>[ShapePermeableY] セル ([Shape Layout] セクション)

コネクタの接続経路が、配置可能な図形上を垂直方向に通過するかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |コネクタの接続経路は、配置可能な図形上を垂直方向に通過します。  <br/> |
|FALSE  <br/> |コネクタの接続経路は、配置可能な図形上を垂直方向に通過できません。  <br/> |
   
## <a name="remarks"></a>注釈

[動作] ダイアログ ボックスの [配置] タブで、このセルの値を設定することもできます (図形が選択されている場合は、[開発] タブの[図形のデザイン] グループで、[動作] をクリックし、[配置] タブ **をクリック** します)。  [](run-in-developer-mode-display-the-developer-tab.md) 
  
Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePermeableY] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapePermeableY  <br/> |
   
プログラムから、インデックスによって [ShapePermeableY] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPermY** <br/> |
   

