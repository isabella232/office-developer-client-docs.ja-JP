---
title: '[BevelDepthSize] セル ([ベベルのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c6a57e52-c7ed-4a52-940f-1cef9baa70a5
description: 面取りの奥行きのサイズをポイント単位で指定します。
ms.openlocfilehash: 13c00536d6fc4f19ff2c62cab2afd04f9cdf8985
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438499"
---
# <a name="beveldepthsize-cell-bevel-properties-section"></a>[BevelDepthSize] セル ([ベベルのプロパティ] セクション)

面取りの奥行きのサイズをポイント単位で指定します。 
  
## <a name="remarks"></a>注釈

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[beveldepthsize]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [beveldepthsize]  <br/> |
   
プログラムから、インデックスによって [ **[beveldepthsize]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowBevelProperties** <br/> |
| セル インデックス:  <br/> |**visBevelDepthSize** <br/> |
   

