---
title: '[BevelMaterialType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: 傾斜面で構成する材料のタイプを決定します。
ms.openlocfilehash: cd4ab223754ffcf7f46478cbc65faff373a3d692
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19804836"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>[BevelMaterialType] セル ([ベベルのプロパティ] セクション)

傾斜面で構成する材料のタイプを決定します。 
  
|**説明**|**値**|
|:-----|:-----|
|0  <br/> |しない特殊な素材  <br/> |
|1  <br/> |つや消し  <br/> |
|2  <br/> |つや消し (明るめ)  <br/> |
|3  <br/> |プラスチック  <br/> |
|4  <br/> |メタル  <br/> |
|5  <br/> |ダーク エッジ  <br/> |
|6  <br/> |ぼかし  <br/> |
|7  <br/> |フラット  <br/> |
|8  <br/> |ワイヤーフレーム  <br/> |
|9  <br/> |パウダー  <br/> |
|10  <br/> |透明パウダー  <br/> |
|11  <br/> |透明  <br/> |
   
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **BevelMaterialType** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | BevelMaterialType  <br/> |
   
プログラムから、インデックスによって [ **BevelMaterialType** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowBevelProperties** <br/> |
| セル インデックス:  <br/> |**visBevelMaterialType** <br/> |
   

