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
ms.openlocfilehash: 6bc1629c51fc4dcb3fe7e2d6576e8f1f096144ae
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805917"
---
# <a name="name-cell-reviewer-section"></a>[Name] セル ([レビュー担当者] セクション)

図面校閲者の名前が含まれます。
  
## <a name="remarks"></a>注釈

 デフォルト値は**Visio のオプション**] ダイアログ ボックスの [**全般**] タブに、[**ユーザー名**] ボックスに名前 (、[**ファイル**] タブをクリックして、**オプション**] をクリックし、し、[**全般**] をクリック) します。 
  
取得する Name] セルへの参照を名前で別の数式からまたはプログラムから**CellsU**プロパティを使用して、次のコマンドを使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | Reviewer.Name [ *i* ]、 *i* = < 1 > では、2、3.  <br/> |
   
プログラムから、インデックスによって [Name] セルへの参照を取得するには、**CellsSRC** プロパティを使用して次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionReviewer** <br/> |
| 行インデックス:  <br/> |**visRowReviewer** +  *i* 、 *i* = 0, 1, 2.  <br/> |
| セル インデックス:  <br/> |**visReviewerName** <br/> |
   

