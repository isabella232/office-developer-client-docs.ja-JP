---
title: '[Name] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
ms.localizationpriority: medium
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: 図面校閲者の名前が含まれます。
ms.openlocfilehash: 7f04882b5b5ba8bfed3a275b3700164c52d23cf4
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563022"
---
# <a name="name-cell-reviewer-section"></a>[Name] セル ([Reviewer] セクション)

図面校閲者の名前が含まれます。
  
## <a name="remarks"></a>注釈

 この値の既定値は **、[Visio** オプション]ダイアログ ボックスの[全般] タブの [ユーザー名] ボックスにある名前です([ファイル] タブをクリックし、[オプション] をクリックし、[全般] をクリック **します)。** 
  
別の数式または **CellsU** プロパティを使用してプログラムから名前によって [名前] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Reviewer.Name [  *i*  ] ここで  *、i*  = <1>、2、3..  <br/> |
   
プログラムから、インデックスによって [Name] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer**  +  *i* *=* 0, 1, 2...  <br/> |
| セル インデックス:  <br/> |**visReviewerName** <br/> |
   

