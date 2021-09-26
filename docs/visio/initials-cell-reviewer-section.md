---
title: '[Initials] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
ms.localizationpriority: medium
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: 図面の校閲者の頭文字を格納します。
ms.openlocfilehash: e3f76685631ca6ddba1848d8ecd57533755ecf84
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59618806"
---
# <a name="initials-cell-reviewer-section"></a>[Initials] セル ([Reviewer] セクション)

図面の校閲者の頭文字を格納します。
  
## <a name="remarks"></a>注釈

この値の既定値は **、[Visio** オプション]ダイアログ ボックスの[全般] タブの [イニシャル]ボックスのイニシャルです ([ファイル] タブをクリックし、[オプション] をクリックし、[全般] をクリック **します**)。  
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Initials] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Reviewer.Initials [  *i*  ] ここで  *、i*  = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Initials] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visReviewerInitials** <br/> |
   

