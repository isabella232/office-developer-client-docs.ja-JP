---
title: '[VariationColorIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea95a90c-4729-4689-a6f4-31dfccf37b9b
description: 整数値としてページで、アクティブなテーマのバリエーションの色のインデックスを決定します。
ms.openlocfilehash: b61317bc9048a6263e217e3eb29dc4dedcd911d8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806753"
---
# <a name="variationcolorindex-cell-theme-properties-section"></a>[VariationColorIndex] セル ([テーマのプロパティ] セクション)

整数値としてページで、アクティブなテーマのバリエーションの色のインデックスを決定します。
  
## <a name="remarks"></a>備考

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **VariationColorIndex** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | VariationColorIndex  <br/> |
   
プログラムから、インデックスによって [ **VariationColorIndex** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowThemeProperties** <br/> |
| セル インデックス:  <br/> |**visVariationColorIndex** <br/> |
   

