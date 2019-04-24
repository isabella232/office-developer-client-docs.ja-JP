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
description: '[レイアウトの構成] ダイアログボックスでレイアウトを構成するときに、表示されていない内部のページグリッドに基づいて、アプリケーションで図形をレイアウトするかどうかを指定します。 ([デザイン] タブの [レイアウト] で [ページの再レイアウト] をクリックし、[その他のレイアウトオプション] をクリックします)。'
ms.openlocfilehash: 11299ca7c9b0ea050542baf97e2cab3a27fa52ba
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345557"
---
# <a name="enablegrid-cell-page-layout-section"></a>[EnableGrid] セル ([Page Layout] セクション)

[**レイアウトの構成**] ダイアログ ボックスでレイアウトを構成するときに、表示されない内部的なページ グリッドを基準にして図形をレイアウトするかどうかを指定します (このダイアログ ボックスを開くには、[**デザイン**] タブの [**レイアウト**] グループで、[**ページの再レイアウト**] をクリックして、[**その他のレイアウト オプション**] をクリックします)。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |内部ページ グリッドを使用します。  <br/> |
|FALSE  <br/> |内部ページ グリッドを使用しません。  <br/> |
   
## <a name="remarks"></a>解説

このページ グリッドは、[**間隔と図形サイズの設定**] ダイアログ ボックスの [**図形の間隔**] と [**図形の平均サイズ**] の値を使用して作成します (このダイアログ ボックスを開くには、[**デザイン**] タブで [**ページ設定**] 矢印をクリックし、[**レイアウトと経路**]、[**間隔**] の順にクリックします)。 
  
この機能を有効にすると、配置可能な各図形の中心点が、内部ページ グリッドのブロックの中心に合わせて整列します。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableGrid] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[enablegrid]  <br/> |
   
プログラムから、インデックスによって [EnableGrid] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOEnableGrid** <br/> |
   

