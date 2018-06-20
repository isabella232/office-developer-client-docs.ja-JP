---
title: '[OnPage] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
localization_priority: Normal
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: 特定のプリンター ページ番号に図面を印刷するかどうかを示します。
ms.openlocfilehash: 5b695ccf6fa2364809e2f5124b9f55ea6aab50e0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805936"
---
# <a name="onpage-cell-print-properties-section"></a>[OnPage] セル ([Print Properties] セクション)

特定のプリンター ページ番号に図面を印刷するかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |プリンター ページの数を定義する図面ページに合わせてください。  <br/> |
|FALSE  <br/> |プリンター ページを定義済みの図面ページ番号に合わせません。  <br/> |
   
## <a name="remarks"></a>注釈

[OnPage] セルが TRUE に設定されている場合は、[PagesX] セルおよび [PagesY] セルを使用して、図面に合うプリンター ページ番号が特定されます。[ScaleX] セルおよび [ScaleY] セル内の値は無視されます。これは "自動サイズ" 設定と見なすことができます。
  
この値**に合わせる**] オプション、[**ページ設定**] ダイアログ ボックスの [**印刷設定**] タブ上に対応 ([**デザイン**] タブで、矢印をクリック、 **[ページ設定**)。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [onpage] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[Onpage]  <br/> |
   
プログラムから、インデックスによって [onpage] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

