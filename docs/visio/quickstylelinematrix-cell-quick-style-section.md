---
title: '[QuickStyleLineMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3b10221d-30f8-48f5-81ed-0283fdfc3e5d
description: 図形が継承するクイックスタイルの線のスタイルを、0-6 からの整数で指定します。
ms.openlocfilehash: e04fc6328d40b0564364aa8feff971628360d813
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282587"
---
# <a name="quickstylelinematrix-cell-quick-style-section"></a>[QuickStyleLineMatrix] セル ([クイック スタイル] セクション)

図形が継承するクイックスタイルの線のスタイルを、0-6 からの整数で指定します。 
  
## <a name="remarks"></a>解説

別の数式から、 **cell**要素の**N**属性の値によって、または**CellsU**プロパティを使用したプログラムから、名前によって [ **[quickstylelinematrix]** ] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | [quickstylelinematrix]  <br/> |
   
プログラムから、インデックスによって [ **[quickstylelinematrix]** ] セルへの参照を取得するには、 **CellsSRC**プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleLineMatrix** <br/> |
   

