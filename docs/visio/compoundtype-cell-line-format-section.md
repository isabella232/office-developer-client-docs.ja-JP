---
title: '[CompoundType] セル ([線の形式] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: 図形の線の複合型を決定します。
ms.openlocfilehash: c43175bc42e74bc18b8bf643976fdc859e3dbf8b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608460"
---
# <a name="compoundtype-cell-line-format-section"></a>[CompoundType] セル ([線の形式] セクション)

図形の線の複合型を決定します。 
  
|**値**|**説明**|
|:-----|:-----|
|0  <br/> |Simple/標準  <br/> |
|1  <br/> |Double  <br/> |
|2  <br/> |太い薄い  <br/> |
|3  <br/> |薄い太さ  <br/> |
|4   <br/> |Triple  <br/> |
   
## <a name="remarks"></a>注釈

別の数式、Cell 要素 **の N** 属性の値、**または CellsU** プロパティを使用するプログラムから、名前によって **[CompoundType]** セルへの参照を取得するには、次の値を使用します。  
  
|||
|:-----|:-----|
| セル名:  <br/> | CompoundType  <br/> |
   
プログラムからインデックスによって **[CompoundType]** セルへの参照を取得するには **、CellsSRC** プロパティを使用して、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visCompoundType** <br/> |
   

