---
title: '[Color] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60032
localization_priority: Normal
ms.assetid: c1e3d7bf-e6b6-65f1-ae40-80c8ba4821cd
description: 図面校閲者のマークアップに割り当てられている色を表す RGB 値。
ms.openlocfilehash: d9df6605ca6c8a22353978b9483989ecfc08130d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430540"
---
# <a name="color-cell-reviewer-section"></a>[Color] セル ([Reviewer] セクション)

図面校閲者のマークアップに割り当てられている色を表す RGB 値。 
  
## <a name="remarks"></a>注釈

色は、赤、青、緑、紫、オレンジ、青緑、グレーの順番で校閲者に割り当てられます。校閲者がそれ以上いる場合には、再度先頭から順番に割り当てられます。 
  
オリジナルの図面ページに記入されたコメントは、[Color] セルで校閲者に割り当てた色にかかわらず常に黄色です。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Color] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | 校閲者の色 [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Color] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visReviewerColor** <br/> |
   

