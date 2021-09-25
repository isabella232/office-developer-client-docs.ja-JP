---
title: '[DrawingScaleType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
ms.localizationpriority: medium
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: '[ページ設定] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[ホーム] タブで [ページ設定] 矢印をクリックします)。'
ms.openlocfilehash: 9cd48ab970b9de0987c655705cc86060ced5cbdb
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59590234"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>[DrawingScaleType] セル ([Page Properties] セクション)

[**ページ設定**] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[**ホーム**] タブで [**ページ設定**] 矢印をクリックします)。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 等倍  <br/> |**visNoScale** <br/> |
| 1  <br/> | 建築系縮尺  <br/> |**visArchitectural** <br/> |
| 2  <br/> | 土木系縮尺  <br/> |**visEngineering** <br/> |
| 3  <br/> | ユーザー設定の縮尺  <br/> |**visScaleCustom** <br/> |
| 4   <br/> | 測定基準  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | 機械系縮尺  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingScaleType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | DrawingScaleType  <br/> |
   
プログラムから、インデックスによって [DrawingScaleType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageDrawScaleType** <br/> |
   

