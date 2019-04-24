---
title: '[DrawingScaleType] セル ([Page Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm270
localization_priority: Normal
ms.assetid: 5d4f1cf8-bc1f-07b8-1da5-7253808e337e
description: '[ページ設定] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[ホーム] タブで [ページ設定] 矢印をクリックします)。'
ms.openlocfilehash: d1c1c00ffe025c566646a1f8b9fe034732ad86a8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359690"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>[DrawingScaleType] セル ([Page Properties] セクション)

[**ページ設定**] ダイアログ ボックスで選択される図面縮尺を指定します (このダイアログ ボックスを開くには、[**ホーム**] タブで [**ページ設定**] 矢印をクリックします)。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| .0  <br/> | 等倍  <br/> |**visNoScale** <br/> |
| 1-d  <br/> | 建築系縮尺  <br/> |**visArchitectural** <br/> |
| pbm-2  <br/> | 土木系縮尺  <br/> |**visEngineering** <br/> |
| 1/3  <br/> | ユーザー設定の縮尺  <br/> |**visScaleCustom** <br/> |
| 2/4  <br/> | 測定基準  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | 機械系縮尺  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [DrawingScaleType] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | [drawingscaletype]  <br/> |
   
プログラムから、インデックスによって [DrawingScaleType] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**vispagedrawetype etype** <br/> |
   

