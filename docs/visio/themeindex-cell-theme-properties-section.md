---
title: '[ThemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: ドキュメントに適用される組み込みの Microsoft Visioテーマの列挙を整数として格納します。 新しいテーマをドキュメント用に選択した場合、ドキュメントの [ThemeIndex] セルとそこに格納されたすべてのページと図形が、組み込みテーマのインデックスを使用して更新されます。
ms.openlocfilehash: a016fdef87fd0324b71cb912482fa9f1d797b946
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603306"
---
# <a name="themeindex-cell-theme-properties-section"></a>[ThemeIndex] セル ([テーマのプロパティ] セクション)

ドキュメントに適用される組み込みの Microsoft Visioテーマの列挙を整数として格納します。 新しいテーマをドキュメント用に選択した場合、ドキュメントの [**ThemeIndex**] セルとそこに格納されたすべてのページと図形が、組み込みテーマのインデックスを使用して更新されます。 
  
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**ThemeIndex**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ThemeIndex  <br/> |
   
プログラムから、インデックスによって [**ThemeIndex**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowThemeProperties** <br/> |
| セル インデックス:  <br/> |**visThemeIndex** <br/> |
   

