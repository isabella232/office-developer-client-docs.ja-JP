---
title: '[ViewMarkup] セル ([Document Properties] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
ms.localizationpriority: medium
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: 図面ウィンドウに校正履歴を表示するかどうかを指定します。
ms.openlocfilehash: 29a4ec7b1d773e8f9d4fade27cf7d000d31a2c54
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59597731"
---
# <a name="viewmarkup-cell-document-properties-section"></a>[ViewMarkup] セル ([Document Properties] セクション

図面ウィンドウに校正履歴を表示するかどうかを指定します。 
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |図面ウィンドウに校正履歴を表示します。  <br/> |
|FALSE  <br/> |校正履歴を表示しません (既定値)。  <br/> |
   
## <a name="remarks"></a>注釈

 マークアップ追跡が有効になっている場合 (AddMarkup セルが TRUE の場合)、ViewMarkup セルは自動的に TRUE に設定され、マークアップ追跡がオフになっても TRUE のままです (AddMarkup セルは FALSE です)。 [AddMarkup] セルが TRUE の場合、[ViewMarkup] セル内の値は無視されます。 
  
図面にコメントを挿入した場合、校正履歴の記録機能がオンかどうかに関わらず、[ViewMarkup] セルは TRUE に設定されます。[ViewMarkup] セルが TRUE でなければ、図面内にコメントが表示されません。
  
このセルは、[**校閲**] タブの [**校正履歴**] グループにある [**変更履歴とコメントの表示**] コマンドに対応しています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [ViewMarkup] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |ViewMarkup  <br/> |
   
プログラムから、インデックスによって [ViewMarkup] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowDoc** <br/> |
|セル インデックス:  <br/> |**visDocViewMarkup** <br/> |
   

