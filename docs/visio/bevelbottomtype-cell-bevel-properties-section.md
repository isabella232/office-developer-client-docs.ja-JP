---
title: '[BevelBottomType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ac7b39d4-3942-4b23-b188-2c3f69e54929
description: 図形の面取りの下面取りの種類を指定します。
ms.openlocfilehash: 0cd360f633145c7dea95438ffe2bc746e519ce13
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330080"
---
# <a name="bevelbottomtype-cell-bevel-properties-section"></a>[BevelBottomType] セル ([ベベルのプロパティ] セクション)

図形の面取りの下面取りの種類を指定します。
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |ベベルなし  <br/> |
|1-d  <br/> |円ベベル  <br/> |
|pbm-2  <br/> |額縁風ベベル  <br/> |
|1/3  <br/> |クロス ベベル  <br/> |
|2/4  <br/> |クール スラント ベベル  <br/> |
|5  <br/> |アングル ベベル  <br/> |
|シックス  <br/> |ソフト ラウンド ベベル  <br/> |
|7  <br/> |凸面ベベル  <br/> |
|~  <br/> |スロープ ベベル  <br/> |
|i-9  <br/> |切り込みベベル  <br/> |
|個  <br/> |スケール ベベル  <br/> |
|#  <br/> |ハード エッジ ベベル  <br/> |
|個  <br/> |アール デコ ベベル  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、**Cell** エレメントの **N** 属性の値 (.vsdx 形式) によって、または**CellsU** プロパティを使用したプログラムから、名前によって [**BevelBottomType**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | BevelBottomType  <br/> |
   
プログラムから、インデックスによって [**BevelBottomType**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowBevelProperties** <br/> |
| セル インデックス:  <br/> |**visBevelBottomType** <br/> |
   

