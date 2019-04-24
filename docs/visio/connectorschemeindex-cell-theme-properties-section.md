---
title: '[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 48ab98bd-2966-443c-b3db-befeb271550f
description: 図形に適用されるテーマのコネクタスキームを整数で指定します。
ms.openlocfilehash: 77d16632db63d187477ba62a1a6f4b9319e156fc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319713"
---
# <a name="connectorschemeindex-cell-theme-properties-section"></a>[ConnectorSchemeIndex] セル ([テーマのプロパティ] セクション)

図形に適用されるテーマのコネクタスキームを整数で指定します。 
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[connectorschemeindex]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [connectorschemeindex]  <br/> |
   
プログラムから、インデックスによって [ **[connectorschemeindex]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowThemeProperties** <br/> |
| セル インデックス:  <br/> |* * visConnectorSchemeIndex * * <br/> |
   

