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
description: ドキュメントの校閲者のマークアップに割り当てられた色を表す RGB 値です。
ms.openlocfilehash: a8771bb35cfc1b57990f24e1a0a3d677f9cffc0b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805030"
---
# <a name="color-cell-reviewer-section"></a>[Color] セル ([Reviewer] セクション)

ドキュメントの校閲者のマークアップに割り当てられた色を表す RGB 値です。 
  
## <a name="remarks"></a>備考

色は、赤、青、緑、紫、オレンジ、青緑、グレーの順番で校閲者に割り当てられます。校閲者がそれ以上いる場合には、再度先頭から順番に割り当てられます。 
  
オリジナルの図面ページに記入されたコメントは、[Color] セルで校閲者に割り当てた色にかかわらず常に黄色です。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Color] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Reviewer.Color [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Color] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visReviewerColor** <br/> |
   

