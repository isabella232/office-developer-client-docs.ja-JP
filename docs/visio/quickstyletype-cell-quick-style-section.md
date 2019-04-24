---
title: '[QuickStyleType] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e7470417-0d70-433e-9496-604ca2eafee6
description: 図形が継承するクイックスタイルの種類 (2 次元、1次元、またはコネクタ) を指定します。
ms.openlocfilehash: 95aced62c6397fc3229de29b98d3f18e5f69d05b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282580"
---
# <a name="quickstyletype-cell-quick-style-section"></a>[QuickStyleType] セル ([クイック スタイル] セクション)

図形が継承するクイックスタイルの種類 (2 次元、1次元、またはコネクタ) を指定します。 
  
|**値**|**説明**|
|:-----|:-----|
|.0  <br/> |Visio が自動的に選択する  <br/> |
|1-d  <br/> |1次元  <br/> |
|pbm-2  <br/> |2次元  <br/> |
|1/3  <br/> |Connector  <br/> |
   
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [**クイックスタイルの種類**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [quickstyletype]  <br/> |
   
プログラムから、インデックスによって [**クイックスタイルの種類**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleType** <br/> |
   

