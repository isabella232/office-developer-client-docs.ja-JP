---
title: '[EnableGrid] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251642
ms.localizationpriority: medium
ms.assetid: bfea4ef4-1b30-eb22-215d-3b9b73098da9
description: '[レイアウトの構成] ダイアログ ボックスでレイアウトを構成するときに、表示されない内部的なページ グリッドを基準にして図形をレイアウトするかどうかを指定します (このダイアログ ボックスを開くには、[デザイン] タブの [レイアウト] グループで、[ページの再レイアウト] をクリックして、[その他のレイアウト オプション] をクリックします)。'
ms.openlocfilehash: f80678446fdb270149f55b2d537237108c9d54f9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570716"
---
# <a name="enablegrid-cell-page-layout-section"></a>[EnableGrid] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログ ボックスでレイアウトを構成するときに、表示されない内部的なページ グリッドを基準にして図形をレイアウトするかどうかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |内部ページ グリッドを使用します。  <br/> |
|FALSE  <br/> |内部ページ グリッドを使用しません。  <br/> |
   
## <a name="remarks"></a>注釈

このページ グリッドは、[**間隔と図形サイズの設定**] ダイアログ ボックスの [**図形の間隔**] と [**図形の平均サイズ**] の値を使用して作成します (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**]、[**間隔**] の順にクリックします)。 
  
この機能を有効にすると、配置可能な各図形の中心点が、内部ページ グリッドのブロックの中心に合わせて整列します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableGrid] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |EnableGrid  <br/> |
   
プログラムから、インデックスによって [EnableGrid] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOEnableGrid** <br/> |
   

