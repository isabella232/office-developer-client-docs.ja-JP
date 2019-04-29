---
title: '[Name] セル ([Reviewer] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1030992
localization_priority: Normal
ms.assetid: be39cd0b-56bf-a070-f5d8-c9a440d81ee2
description: 図面校閲者の名前が含まれます。
ms.openlocfilehash: 02f353ab8f2d39cc075211bb13157b93081e9d8f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417687"
---
# <a name="name-cell-reviewer-section"></a>[Name] セル ([Reviewer] セクション)

図面校閲者の名前が含まれます。
  
## <a name="remarks"></a>注釈

 この値の既定値は、[ **Visio のオプション**] ダイアログボックス ([**ファイル**] タブをクリックし、[**オプション**] をクリックし、[**全般**] をクリック) の [**全般**] タブの [**ユーザー名**] ボックスにある名前です。 
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって [name] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Reviewer.Name [ *i* ] *i* = <1>、2、3...  <br/> |
   
プログラムから、インデックスによって [Name] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer** +  *i* = ** 0、1、2...  <br/> |
| セル インデックス:  <br/> |**visReviewerName** <br/> |
   

