---
title: '[ShapePermeablePlace] セル ([Shape Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm885
localization_priority: Normal
ms.assetid: b647cbb5-2769-068d-bbda-2dc983c47ac9
description: '[レイアウトの構成] ダイアログ ボックスで図形をレイアウトするときに、配置可能な図形を図形の上部に配置するかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: 1873575eb4322d31f81c0dd34557c6167750ce82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806395"
---
# <a name="shapepermeableplace-cell-shape-layout-section"></a>[ShapePermeablePlace] セル ([図形レイアウト] セクション)

[**レイアウトの構成**] ダイアログ ボックスで図形をレイアウトするときに、配置可能な図形を図形の上部に配置するかどうかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |他図形をこの図形の上に配置できます。  <br/> |
|FALSE  <br/> |他図形をこの図形の上に配置できません。  <br/> |
   
## <a name="remarks"></a>注釈

**動作**] ダイアログ ボックスの [**配置**] タブで、このセルの値を設定することもできます (図形を選択して、[[開発](run-in-developer-mode-display-the-developer-tab.md)] タブの [**図形のデザイン**] で、[**動作**] をクリックし、[**配置**] タブをクリックして). 
  
Visio 2000 より前のバージョンでは、[Miscellaneous] セクションで [ObjInteract] セルを使用してこの動作を設定していました。
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ShapePermeablePlace] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ShapePermeablePlace  <br/> |
   
プログラムから、インデックスによって [ShapePermeablePlace] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowShapeLayout** <br/> |
|セル インデックス:  <br/> |**visSLOPermeablePlace** <br/> |
   

