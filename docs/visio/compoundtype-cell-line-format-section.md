---
title: '[CompoundType] セル ([線の形式] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3e2a88ad-d92c-4550-8da3-fa7fdd032e73
description: 図形の線の複合型を指定します。
ms.openlocfilehash: 120975e419656234266cb8151b2fa37ef19602e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359371"
---
# <a name="compoundtype-cell-line-format-section"></a>[CompoundType] セル ([線の形式] セクション)

図形の線の複合型を指定します。 
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |Simple/標準  <br/> |
|1-d  <br/> |倍精度浮動小数点数  <br/> |
|pbm-2  <br/> |太線 (細)  <br/> |
|1/3  <br/> |細い太線  <br/> |
|2/4  <br/> |Triple  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[compoundtype]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [compoundtype]  <br/> |
   
プログラムから、インデックスによって [ **[compoundtype]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visCompoundType** <br/> |
   

