---
title: '[BevelTopType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e29af0d-4183-41d1-8b0f-96450089f882
description: 図形の上端にあるベベルの種類を指定します。
ms.openlocfilehash: 225600a3e39ec58622bcd8597e1115a52cb62a3f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421495"
---
# <a name="beveltoptype-cell-bevel-properties-section"></a>[BevelTopType] セル ([ベベルのプロパティ] セクション)

図形の上端にあるベベルの種類を指定します。 
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |ベベルなし  <br/> |
|1   <br/> |円ベベル  <br/> |
|2   <br/> |額縁風ベベル  <br/> |
|3   <br/> |クロス ベベル  <br/> |
|4   <br/> |クール スラント ベベル  <br/> |
|5   <br/> |アングル ベベル  <br/> |
|6   <br/> |ソフト ラウンド ベベル  <br/> |
|7   <br/> |凸面ベベル  <br/> |
|8   <br/> |スロープ ベベル  <br/> |
|9   <br/> |切り込みベベル  <br/> |
|10   <br/> |スケール ベベル  <br/> |
|11   <br/> |ハード エッジ ベベル  <br/> |
|12   <br/> |アール デコ ベベル  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**BevelTopType**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |BevelTopType  <br/> |
   
プログラムから、インデックスによって [**BevelTopType**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowBevelProperties** <br/> |
|セル インデックス:  <br/> |**visBevelTopType** <br/> |
   

