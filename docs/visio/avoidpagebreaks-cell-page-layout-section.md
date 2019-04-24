---
title: '[AvoidPageBreaks] セル ([Page Layout] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80000
localization_priority: Normal
ms.assetid: 7d2ec869-7ffa-3b41-8126-3f4889501e0c
description: 図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。
ms.openlocfilehash: 5ff5a31e26cc1ab9415eb69b76fc9f64ccd1ae7d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338725"
---
# <a name="avoidpagebreaks-cell-page-layout-section"></a>[AvoidPageBreaks] セル ([Page Layout] セクション)

図形を整列するか、均等に配置するか、またはその両方を行う場合に、図形を改ページの上に配置できるかどうかを指定します。
  
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [AvoidPageBreaks] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |AvoidPageBreaks  <br/> |
   
プログラムから、インデックスによって [AvoidPageBreaks] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowPageLayout** <br/> |
|セル インデックス:  <br/> |**visPLOAvoidPageBreaks** <br/> |
   

