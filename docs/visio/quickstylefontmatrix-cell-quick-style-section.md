---
title: '[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 304ee083-e9c8-45df-b411-ba5e7db4c086
description: 各クイックスタイルのフォントのスタイルを、1 ~ 6 の整数で指定します。
ms.openlocfilehash: 0708a243b001c7b4e03158b5a332a3166727cabc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360075"
---
# <a name="quickstylefontmatrix-cell-quick-style-section"></a>[QuickStyleFontMatrix] セル ([クイック スタイル] セクション)

各クイックスタイルのフォントのスタイルを、1 ~ 6 の整数で指定します。
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [**クイックスタイルのフォントマトリックス**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [quickstylefontmatrix]  <br/> |
   
プログラムから、インデックスによって [**クイックスタイルのフォントマトリックス**] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleFontMatrix** <br/> |
   

