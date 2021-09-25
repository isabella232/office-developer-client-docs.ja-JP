---
title: '[Height] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251195
ms.localizationpriority: medium
ms.assetid: 194d5beb-c705-f567-84de-8305c41081a8
description: 図形の高さを図面単位で指定します。
ms.openlocfilehash: 27c1c7fb17cf392d6d3ecad7090d4c4ade95005a
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628242"
---
# <a name="height-cell-shape-transform-section"></a>[Height] セル ([Shape Transform] セクション)

図形の高さを図面単位で指定します。
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Height] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Height  <br/> |
   
プログラムから、インデックスによって [Height] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormHeight** <br/> |
   

