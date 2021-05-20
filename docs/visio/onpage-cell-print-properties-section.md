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
ms.openlocfilehash: 61d45a5bffdbb1afd5db9c608f80bc4f797f5191
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439605"
---
# <a name="onpage-cell-print-properties-section"></a>[OnPage] セル ([Print Properties] セクション)

特定のプリンター ページ番号に図面を印刷するかどうかを示します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図面ページを定義済みのプリンター ページ数に合わせて指定します。  <br/> |
|FALSE  <br/> |プリンター ページを定義済みの図面ページ番号に合わせません。  <br/> |
   
## <a name="remarks"></a>注釈

[OnPage] セルが TRUE に設定されている場合は、[PagesX] セルおよび [PagesY] セルを使用して、図面に合うプリンター ページ番号が特定されます。[ScaleX] セルおよび [ScaleY] セル内の値は無視されます。これは "自動サイズ" 設定と見なすことができます。
  
この値は、[ページセットアップ] ダイアログ ボックスの [印刷設定] タブの [適合] オプションに対応します ([デザイン] タブの [ページ設定] 矢印 **をクリック** します)。  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [OnPage] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |OnPage  <br/> |
   
プログラムから、インデックスによって [OnPage] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPrintProperties** <br/> |
|セル インデックス:  <br/> |**visPrintPropertiesOnPage** <br/> |
   

