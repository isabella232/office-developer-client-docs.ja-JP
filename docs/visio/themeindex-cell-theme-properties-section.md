---
title: '[ThemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21002267-1400-4398-b937-f5b289cf0ed2
description: 整数として、ドキュメントに適用される組み込みの Microsoft Visio のテーマの列挙体を格納します。 ドキュメントの新しいテーマを選択すると、組み込みのテーマのインデックスを使用してドキュメントとすべてのページと図形が含まれているの ThemeIndex のセルが更新されます。
ms.openlocfilehash: 8a9202631bc4d9131d52dea1f852983e1d7528e5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806636"
---
# <a name="themeindex-cell-theme-properties-section"></a>[ThemeIndex] セル ([テーマのプロパティ] セクション)

整数として、ドキュメントに適用される組み込みの Microsoft Visio のテーマの列挙体を格納します。 ドキュメント、ドキュメントの**ThemeIndex**のセルに新しいテーマを選択したし、組み込みのテーマのインデックスを持つすべてのページとそれに含まれる図形が更新されます。 
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **ThemeIndex** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | ThemeIndex  <br/> |
   
プログラムから、インデックスによって [ **ThemeIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowThemeProperties** <br/> |
| セル インデックス:  <br/> |**visThemeIndex** <br/> |
   

