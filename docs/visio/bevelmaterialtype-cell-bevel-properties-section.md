---
title: '[BevelMaterialType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: ベベルを構成する素材の種類を指定します。
ms.openlocfilehash: b8efaa1f84594c803c79be02cd88dda1a5346dc7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315765"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>[BevelMaterialType] セル ([ベベルのプロパティ] セクション)

ベベルを構成する素材の種類を指定します。 
  
|**説明**|**値**|
|:-----|:-----|
|.0  <br/> |特別な素材なし  <br/> |
|1-d  <br/> |つや消し  <br/> |
|pbm-2  <br/> |つや消し (明るめ)  <br/> |
|1/3  <br/> |プラスチック  <br/> |
|2/4  <br/> |メタル  <br/> |
|5  <br/> |ダークエッジ  <br/> |
|シックス  <br/> |ぼかし  <br/> |
|7  <br/> |[Flat/なし]  <br/> |
|~  <br/> |ワイヤーフレーム  <br/> |
|i-9  <br/> |パウダー  <br/> |
|個  <br/> |透明パウダー  <br/> |
|#  <br/> |Clear  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[bevelmaterialtype]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [bevelmaterialtype]  <br/> |
   
プログラムから、インデックスによって [ **[bevelmaterialtype]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowBevelProperties** <br/> |
| セル インデックス:  <br/> |**visBevelMaterialType** <br/> |
   

