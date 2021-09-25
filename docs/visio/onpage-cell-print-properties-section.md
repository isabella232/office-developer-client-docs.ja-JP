---
title: '[OnPage] セル ([Print Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033793
ms.localizationpriority: medium
ms.assetid: 4015506a-e24a-0276-c854-7791a7019067
description: 特定のプリンター ページ番号に図面を印刷するかどうかを示します。
ms.openlocfilehash: 265d5d02b17feddd8d7ff1865ec9ae2fbf7f355e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590192"
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
   

