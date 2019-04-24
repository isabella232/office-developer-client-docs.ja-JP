---
title: '[Initials] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60045
localization_priority: Normal
ms.assetid: 8f5d34f0-4c4b-5265-83c1-5b86b73d464f
description: 図面の校閲者の頭文字を格納します。
ms.openlocfilehash: ddca3697dfcf1f422efacbe395c18f1a6b8ac48c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335295"
---
# <a name="initials-cell-reviewer-section"></a>[Initials] セル ([Reviewer] セクション)

図面の校閲者の頭文字を格納します。
  
## <a name="remarks"></a>解説

この値の既定値は、[ **** **Visio のオプション**] ダイアログボックス ([**ファイル**] タブをクリックし、[**オプション**] をクリックし、[**全般**] をクリックします) の [**全般**] タブの [イニシャル] ボックスに設定されています。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [Initials] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | レビューアー [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Initials] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visReviewerInitials** <br/> |
   

