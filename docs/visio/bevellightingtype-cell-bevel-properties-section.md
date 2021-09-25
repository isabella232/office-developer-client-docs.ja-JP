---
title: '[BevelLightingType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7fbb4b16-fe54-42d6-803a-c9980897166d
description: ベベル効果に使用する光源の種類を決定します。
ms.openlocfilehash: 6cfdf61a8584753417f57df4dcdc3eedfdb4ed33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554888"
---
# <a name="bevellightingtype-cell-bevel-properties-section"></a>[BevelLightingType] セル ([ベベルのプロパティ] セクション)

ベベル効果に使用する光源の種類を決定します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |光源なし  <br/> |
|1  <br/> |3 点  <br/> |
|2  <br/> |残高  <br/> |
|3  <br/> |ソフト  <br/> |
|4   <br/> |厳しい  <br/> |
|5  <br/> |Flood  <br/> |
|6   <br/> |コントラスト  <br/> |
|7   <br/> |朝  <br/> |
|8   <br/> |サンライズ  <br/> |
|9   <br/> |終了する  <br/> |
|10  <br/> |肌寒い  <br/> |
|11  <br/> |フリーズ  <br/> |
|12   <br/> |[Flat/なし]  <br/> |
|13  <br/> |2 点  <br/> |
|14   <br/> |Glow  <br/> |
|15   <br/> |明るい室内  <br/> |
   
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素の **N** 属性の値、または **CellsU** プロパティを使用するプログラムから、名前によって **[BevelLightingType]** セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |BevelLightingType  <br/> |
   
プログラムからインデックスによって **[BevelLightingType]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowBevelProperties** <br/> |
|セル インデックス:  <br/> |**visBevelLightingType** <br/> |
   

