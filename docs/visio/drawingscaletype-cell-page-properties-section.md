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
description: '[ページ設定] ダイアログ ボックスで選択した図面の縮尺を指定 ([ホーム] タブの [ページ設定の矢印] をクリック) します。'
ms.openlocfilehash: b93bd95a30fe5a8a5de15a8e5ea104279cf1bcda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805285"
---
# <a name="drawingscaletype-cell-page-properties-section"></a>[DrawingScaleType] セル ([Page Properties] セクション)

**[ページ設定**] ダイアログ ボックスで選択した図面の縮尺を指定 ([**ホーム**] タブの **[ページ設定**の矢印をクリック) します。 
  
|**値**|**説明**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 等倍  <br/> |**visNoScale** <br/> |
| 1  <br/> | 建築系縮尺  <br/> |**visArchitectural** <br/> |
| 2  <br/> | 土木系縮尺  <br/> |**visEngineering** <br/> |
| 3  <br/> | ユーザー設定の縮尺  <br/> |**visScaleCustom** <br/> |
| 4  <br/> | メートル法  <br/> |**visScaleMetric** <br/> |
| 5  <br/> | 機械系縮尺  <br/> |**visScaleMechanical** <br/> |
   
## <a name="remarks"></a>備考

別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[DrawingScaleType] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | DrawingScaleType  <br/> |
   
プログラムから、インデックスによって [DrawingScaleType] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageDrawScaleType** <br/> |
   

