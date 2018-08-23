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
ms.openlocfilehash: 5917abad653e7aaf40da05eafa3f9f1a90a2cf9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806415"
---
# <a name="shapeplowcode-cell-shape-layout-section"></a>[ShapePlowCode] セル ([図形レイアウト] セクション)

図面ページで、別の配置可能な図形をこの図形の近くにドロップしたときに、この図形を移動して遠ざけるかどうかを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|0  <br/> |ページの指定に従って移動します。  <br/> |**visSLOPlowDefault** <br/> |
|1  <br/> |どの図形も移動しません。  <br/> |**visSLOPlowNever** <br/> |
|2  <br/> |すべての図形が移動します。  <br/> |**visSLOPlowAlways** <br/> |
   
## <a name="remarks"></a>注釈

**動作**] ダイアログ ボックスの [**配置**] タブで特定の図形のセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、**配置**] タブ)。 
  
図面ページでこの動作を*すべて*の図形を設定するには、ページ レイアウト] セクションで [plowcode] セルを使用します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePlowCode] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapePlowCode  <br/> |
   
プログラムから、インデックスによって [ShapePlowCode] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPlowCode** <br/> |
   

