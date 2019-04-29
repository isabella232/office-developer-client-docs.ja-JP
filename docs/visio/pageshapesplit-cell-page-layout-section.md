---
title: '[PageShapeSplit] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1033777
localization_priority: Normal
ms.assetid: 4d3bdf77-0ad4-86a4-d215-1d5a5fbe33f7
description: ページの図形が自動的に分割されるかどうかを示します。
ms.openlocfilehash: 18a40e0876b117556a1e7ab43f640e798dc248c0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422020"
---
# <a name="pageshapesplit-cell-page-layout-section"></a>[PageShapeSplit] セル ([Page Layout] セクション)

ページの図形が自動的に分割されるかどうかを示します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |図形の自動分割を許可しません。  <br/> |**visPLOSplitNone** <br/> |
|1   <br/> |図形の自動分割を許可します (既定値)。  <br/> |**visPLOSplitAllow** <br/> |
   
## <a name="remarks"></a>注釈

図形の自動分割は、アプリケーション、ページ、および図形の 3 つのレベルで有効または無効にできます。 既定では、アプリケーションレベルとページレベルでスプリットが有効になっています。 図形の既定の設定は、図面の種類によって異なります。 
  
アプリケーションレベルで分割を有効または無効にするには、[ **visio のオプション**] ダイアログボックスの [**詳細**設定] タブにある [**コネクタ分割を有効**にする] 設定を使用します ( **Office**ボタンをクリックし、 **visio**の [**オプション**] をクリックします)。tab キーを押し、[**詳細設定**] をクリックします。 
  
図形レベルで分割を有効または無効にするには、[図形] 図形のセルを参照してください。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [[pageshapesplit]] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[pageshapesplit]  <br/> |
   
プログラムから、インデックスによって [[pageshapesplit]] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOSplit** <br/> |
   

