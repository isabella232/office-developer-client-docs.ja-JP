---
title: '[NoShow] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
ms.localizationpriority: medium
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: 図面ページにパスを表示するかどうかを示します。
ms.openlocfilehash: 7d545fe9526cad6aca87998f7a62cfff0f9a314d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59577809"
---
# <a name="noshow-cell-geometry-section"></a>[NoShow] セル ([Geometry] セクション)

図面ページにパスを表示するかどうかを示します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形座標セクションによって描画されるパスのストロークと塗りつぶしは表示されません。  <br/> |
| FALSE  <br/> | パスのストロークと塗りつぶしは表示されます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoShow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | Geometry  *i*  .NoShow where i =  *<*  1>、2、3...  <br/> |
   
プログラムから、インデックスによって [NoShow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent**  +  *i* *=* 0, 1, 2...  <br/> |
| 行インデックス :  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoShow** <br/> |
   

