---
title: '[BevelMaterialType] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 30f50a94-88dc-41a3-bb46-45c92d6817a4
description: ベベルが構成されるマテリアルの種類を指定します。
ms.openlocfilehash: 31c062ffedc44b015f5a2329b4ca60f872a8361f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578152"
---
# <a name="bevelmaterialtype-cell-bevel-properties-section"></a>[BevelMaterialType] セル ([ベベルのプロパティ] セクション)

ベベルが構成されるマテリアルの種類を指定します。 
  
|**説明**|**値**|
|:-----|:-----|
|0  <br/> |特別な材料なし  <br/> |
|1  <br/> |つや消し  <br/> |
|2  <br/> |つや消し (明るめ)  <br/> |
|3  <br/> |プラスチック  <br/> |
|4   <br/> |メタル  <br/> |
|5  <br/> |濃いエッジ  <br/> |
|6   <br/> |ぼかし  <br/> |
|7   <br/> |[Flat/なし]  <br/> |
|8   <br/> |ワイヤーフレーム  <br/> |
|9   <br/> |パウダー  <br/> |
|10  <br/> |透明パウダー  <br/> |
|11  <br/> |Clear  <br/> |
   
## <a name="remarks"></a>注釈

別の数式 **、Cell** 要素 **の N** 属性の値、または CellsU プロパティを使用するプログラムから、名前によって **[BevelMaterialType]** セルへの参照を取得するには、次の値を使用します。  
  
|||
|:-----|:-----|
| セル名:  <br/> | BevelMaterialType  <br/> |
   
プログラムからインデックスによって **[BevelMaterialType]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowBevelProperties** <br/> |
| セル インデックス:  <br/> |**visBevelMaterialType** <br/> |
   

