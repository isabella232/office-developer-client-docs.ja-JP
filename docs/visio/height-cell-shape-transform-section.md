---
title: '[Height] セル ([Shape Transform] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251195
localization_priority: Normal
ms.assetid: 194d5beb-c705-f567-84de-8305c41081a8
description: 図形の高さを図面単位で指定します。
ms.openlocfilehash: 1f08fec0ec09e4ba77296495defc91b0f1f3a4c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422867"
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
   

