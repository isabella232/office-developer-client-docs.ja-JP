---
title: '[ViewMarkup] セル ([Document Properties] セクション'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030802
localization_priority: Normal
ms.assetid: 6c956266-8266-3312-5a68-cc9d8bdb8cd9
description: 図面ウィンドウに校正履歴を表示するかどうかを指定します。
ms.openlocfilehash: eeccdd0d14bf28630937b0e480822abb6fb19da5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416406"
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
   

