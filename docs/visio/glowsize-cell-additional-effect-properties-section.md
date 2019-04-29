---
title: '[GlowSize] セル ([追加効果のプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ddc7a08-25b8-4903-b0dd-be72d1fa8075
description: 図形の外側の光彩のサイズをポイント単位で指定します。
ms.openlocfilehash: 6d338ebe23b5c5422c7cdc5a72fccb18eefef87e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409532"
---
# <a name="glowsize-cell-additional-effect-properties-section"></a>[GlowSize] セル ([追加効果のプロパティ] セクション)

図形の外側の光彩のサイズをポイント単位で指定します。 
  
## <a name="remarks"></a>注釈

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[glowsize]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [glowsize]  <br/> |
   
プログラムから、インデックスによって [ **[glowsize]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowOtherEffectProperties** <br/> |
| セル インデックス:  <br/> |**visGlowSize** <br/> |
   

