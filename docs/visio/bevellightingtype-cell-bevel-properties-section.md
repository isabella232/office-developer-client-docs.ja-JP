---
title: '[BevelLightingType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7fbb4b16-fe54-42d6-803a-c9980897166d
description: ベベル効果に使用する光源の種類を決定します。
ms.openlocfilehash: 6d92c56b01d192c1df04eecdaca4eb915baebcae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315772"
---
# <a name="bevellightingtype-cell-bevel-properties-section"></a>[BevelLightingType] セル ([ベベルのプロパティ] セクション)

ベベル効果に使用する光源の種類を決定します。
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |光源なし  <br/> |
|1-d  <br/> |3 点  <br/> |
|pbm-2  <br/> |残高  <br/> |
|1/3  <br/> |ソフト  <br/> |
|2/4  <br/> |直射  <br/> |
|5  <br/> |あふれ  <br/> |
|シックス  <br/> |対照的  <br/> |
|7  <br/> |着く  <br/> |
|~  <br/> |サンライズ  <br/> |
|i-9  <br/> |サンセット  <br/> |
|個  <br/> |冷たい  <br/> |
|#  <br/> |固定  <br/> |
|個  <br/> |[Flat/なし]  <br/> |
|スリー  <br/> |2 点  <br/> |
|第  <br/> |Glow  <br/> |
|約  <br/> |明るい室内  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[bevellightingtype]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |[bevellightingtype]  <br/> |
   
プログラムから、インデックスによって [ **[bevellightingtype]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowBevelProperties** <br/> |
|セル インデックス:  <br/> |**visBevelLightingType** <br/> |
   

