---
title: '[FillGradientDir] セル ([グラデーションのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: 塗りつぶしのグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。
ms.openlocfilehash: 1b467798439383da9a18913ae2efc2e4ee5a08ea
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59612835"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a>[FillGradientDir] セル ([グラデーションのプロパティ] セクション)

塗りつぶしのグラデーションの方向を決定します。グラデーションは線形、放射状、角形、またはパスに沿う形を指定できます。 
  
> [!NOTE]
> 線形のグラデーションは、[**FillGradientDir**] セルで指定した追加の角度値を使用する唯一のグラデーションです。他すべてのグラデーションの方向は、事前に設定された列挙型が適用されます。 
  
****

|**値**|**説明**|
|:-----|:-----|
|0  <br/> |線形のグラデーション。[**FillGradientAngle**] セルは、グラデーションの方向を決定します。<br/> |
|1-7  <br/> |放射状のグラデーション。グラデーションは円の中央から外側に向かって拡張されます。  <br/> |
|8-12  <br/> |角形のグラデーション。グラデーションは、角形のフェードを使用して原点から矢印線として拡張されます。  <br/> |
|13  <br/> |パスのグラデーション。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**FillGradientDir**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | FillGradientDir  <br/> |
   
プログラムから、インデックスによって [**FillGradientDir**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowGradientProperties** <br/> |
| セル インデックス:  <br/> |**visFillGradientDir** <br/> |
   

