---
title: '[BevelLightingType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7fbb4b16-fe54-42d6-803a-c9980897166d
description: ベベル効果に使用する光源の種類を決定します。
ms.openlocfilehash: a8e7c2340f96362965d5ecb890fb47427be9e752
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804844"
---
# <a name="bevellightingtype-cell-bevel-properties-section"></a>[BevelLightingType] セル ([ベベルのプロパティ] セクション)

ベベル効果に使用する光源の種類を決定します。
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |光源なし  <br/> |
|1  <br/> |3 点  <br/> |
|2  <br/> |Balance  <br/> |
|3  <br/> |ぼかし  <br/> |
|4  <br/> |直射光  <br/> |
|5  <br/> |拡散光  <br/> |
|6  <br/> |コントラスト  <br/> |
|7  <br/> |朝  <br/> |
|8  <br/> |サンライズ  <br/> |
|9  <br/> |サンセット  <br/> |
|10  <br/> |冷たい  <br/> |
|11  <br/> |寒い  <br/> |
|12  <br/> |Flat/なし  <br/> |
|13  <br/> |2 点  <br/> |
|14  <br/> |光彩  <br/> |
|15  <br/> |明るい室内  <br/> |
   
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelLightingType** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |BevelLightingType  <br/> |
   
プログラムから、インデックスによって [ **BevelLightingType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowBevelProperties** <br/> |
|セル インデックス:  <br/> |**visBevelLightingType** <br/> |
   

