---
title: '[EnableGrid] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
localization_priority: Normal
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: 非表示、内部ページ グリッド ベースのレイアウトの構成] ダイアログ ボックスでレイアウトを構成するときの図形をレイアウトするかどうかを決定します。 ([デザイン] タブの [レイアウト] で、再レイアウト] ページをクリックして、他のレイアウト オプション] をクリックして)
ms.openlocfilehash: 3371767343132219ebc38134b93afd1da46c7a45
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805305"
---
# <a name="enablegrid-cell-page-layout-section"></a>[EnableGrid] セル ([Page Layout] セクション)

非表示、内部ページ グリッド ベースの**レイアウトの構成**] ダイアログ ボックスでレイアウトを構成するときの図形をレイアウトするかどうかを決定します。 ([**デザイン**] タブの [**レイアウト**] で、**ページの再レイアウト**] をクリックして、**他のレイアウト オプション**] をクリックして)
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |内部ページ グリッドを使用します。  <br/> |
|FALSE  <br/> |内部ページ グリッドを使用しません。  <br/> |
   
## <a name="remarks"></a>注釈

このページのグリッドを作成するには、**図形間の間隔**は、**図形の平均サイズ**の値を使用して**レイアウトと間隔**] ダイアログ ボックスをオンにします。 ([**デザイン**] タブで、**ページ設定**の矢印をクリックして、[**レイアウトと経路**、および、[**間隔**] をクリックします。) 
  
この機能を有効にすると、配置可能な各図形の中心点が、内部ページ グリッドのブロックの中心に合わせて整列します。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[EnableGrid] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |EnableGrid  <br/> |
   
プログラムから、インデックスによって [EnableGrid] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOEnableGrid** <br/> |
   

