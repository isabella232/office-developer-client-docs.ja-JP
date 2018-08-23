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
ms.openlocfilehash: ad4d9cf1aa3e541f512bc09ffc38cf03204b3c94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805957"
---
# <a name="noshow-cell-geometry-section"></a>[NoShow] セル ([図形座標] セクション)

図面ページにパスを表示するかどうかを示します。
  
|**値**|**説明**|
|:-----|:-----|
| TRUE  <br/> | 図形座標セクションによって描画されるパスのストロークと塗りつぶしは表示されません。  <br/> |
| FALSE  <br/> | パスのストロークと塗りつぶしは表示されます。  <br/> |
   
## <a name="remarks"></a>備考

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [NoShow] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ジオメトリの*i*です。[Noshow]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [NoShow] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionFirstComponent** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| 行インデックス:  <br/> |**visRowComponent** <br/> |
| セル インデックス:  <br/> |**visCompNoShow** <br/> |
   

