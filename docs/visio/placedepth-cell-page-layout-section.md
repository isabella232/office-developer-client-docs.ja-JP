---
title: '[PlaceDepth] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1230
ms.localizationpriority: medium
ms.assetid: 02c139db-fe67-f550-1d07-8c8a9a4fb427
description: レイアウトを作成する前に図面を分析する方法を指定します。また、レイアウトの種類も指定します。
ms.openlocfilehash: 10c116de99cce8fce65b6949341174aa6a3cf6b4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559781"
---
# <a name="placedepth-cell-page-layout-section"></a>[PlaceDepth] セル ([Page Layout] セクション)

レイアウトを作成する前に図面を分析する方法を指定します。また、レイアウトの種類も指定します。
  
|**値**|**垂直および水平レイアウトの配置の深さ**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | ページの既定値  <br/> |**visPLOPlaceDepthDefault** <br/> |
| 1  <br/> | 中  <br/> |**visPLOPlaceDepthMedium** <br/> |
| 2  <br/> | 深い  <br/> |**visPLOPlaceDepthDeep** <br/> |
| 3  <br/> | 浅い  <br/> |**visPLOPlaceDepthShallow** <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PlaceDepth] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PlaceDepth  <br/> |
   
プログラムから、インデックスによって [PlaceDepth] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPageLayout** <br/> |
| セル インデックス:  <br/> |**visPLOPlaceDepth** <br/> |
   

