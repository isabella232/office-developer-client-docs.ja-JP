---
title: '[PinX] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm790
ms.localizationpriority: medium
ms.assetid: dd88fb8d-3ec3-476a-870d-6642b191496f
description: 図形のピンの x 座標 (回転の中心) を、親の原点との関係で表します。
ms.openlocfilehash: 35aa20d4b41d00bfb61a4d437dc0b4b06f5ed005
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608073"
---
# <a name="pinx-cell-shape-transform-section"></a>[PinX] セル ([Shape Transform] セクション)

図形の  *ピンの x*  座標 (回転の中心) を、親の原点との関係で表します。 
  
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [PinX] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PinX  <br/> |
   
プログラムから、インデックスによって [PinX] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowXFormOut** <br/> |
| セル インデックス:  <br/> |**visXFormPinX** <br/> |
   

