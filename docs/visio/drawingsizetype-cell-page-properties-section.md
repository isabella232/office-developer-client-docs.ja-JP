---
title: '[DrawingSizeType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm275
localization_priority: Normal
ms.assetid: 7fe270e8-0dff-bf1f-dfc0-c0608af79f59
description: 図面のサイズを指定します。
ms.openlocfilehash: 33c85b6c2f0587654038eaec1a9490ca8bd8301b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425450"
---
# <a name="drawingsizetype-cell-page-properties-section"></a>[DrawingSizeType] セル ([Page Properties] セクション)

図面のサイズを指定します。
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
|.0  <br/> |プリンターの用紙サイズに合わせます。  <br/> |**visPrintSetup** <br/> |
|1   <br/> |図面の内容に合わせてページの大きさを変更します。  <br/> |**visTight** <br/> |
|2   <br/> |標準  <br/> |**visStandard** <br/> |
|3   <br/> |ユーザー設定のページ サイズを使用します。  <br/> |**visCustom** <br/> |
|4   <br/> |ユーザー設定の縮尺を使用します。  <br/> |**visLogical** <br/> |
|5   <br/> |メートル法 (ISO) を使用します。  <br/> |**visDSMetric** <br/> |
|6   <br/> |ANSI 工学系を使用します。  <br/> |**visDSEngr** <br/> |
|7   <br/> |ANSI 建築系を使用します。  <br/> |**visDSArch** <br/> |
   
## <a name="remarks"></a>注釈

図面のサイズを設定するには、[**ページ設定**] ダイアログ ボックス ([**デザイン**] タブの [**ページ設定**] 矢印をクリック) を使用します。または、マウスを使用して手動でページのサイズを変更することもできます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingSizeType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[drawingsizetype]  <br/> |
   
プログラムから、インデックスによって [DrawingSizeType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPage** <br/> |
|セル インデックス:  <br/> |**visPageDrawSizeType** <br/> |
   

