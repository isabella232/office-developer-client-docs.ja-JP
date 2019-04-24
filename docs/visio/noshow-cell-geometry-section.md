---
title: '[NoShow] セル ([Geometry] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm735
localization_priority: Normal
ms.assetid: 831075ff-2875-b598-00bb-eb8481fee57b
description: 図面ページにパスを表示するかどうかを示します。
ms.openlocfilehash: bd42b069e6796b107aafaea3080f6970c4f678c5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341084"
---
# <a name="noshow-cell-geometry-section"></a>[NoShow] セル ([Geometry] セクション)

図面ページにパスを表示するかどうかを示します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形座標セクションによって描画されるパスのストロークと塗りつぶしは表示されません。  <br/> |
| FALSE  <br/> | パスのストロークと塗りつぶしは表示されます。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoShow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | ジオメトリ*i*[noshow] where *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [NoShow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* = ** 0、1、2...  <br/> |
| 行インデックス :  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoShow** <br/> |
   

