---
title: '[Default] セル ([Hyperlinks] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251545
localization_priority: Normal
ms.assetid: 0edea0ea-58dd-15da-6d4f-185d40133452
description: 図形またはページの既定のハイパーリンクを指定します。既定のハイパーリンクを設定するには、このセルの値を TRUE に設定します。
ms.openlocfilehash: a8bfc045559a2c2904ae4a97c489248fb6c446c9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805193"
---
# <a name="default-cell-hyperlinks-section"></a>[Default] セル ([Hyperlinks] セクション)

図形またはページの既定のハイパーリンクを指定します。既定のハイパーリンクを設定するには、このセルの値を TRUE に設定します。
  
## <a name="remarks"></a>注釈

図形を選択すると、[**挿入**] タブで、**ハイパーリンク**をクリックすると、ハイパーリンクを選択すると、 **] をクリック**して既定のハイパーリンクを設定することもできます。 既定のハイパーリンクは太字で表示されます。
  
別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[Default] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
|セル名:  <br/> |ハイパーリンク *名*です。既定の場所のハイパーリンクです。 *名前*は、行の名前  <br/> |
   
プログラムから、インデックスによって [Default] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionHyperlink** <br/> |
|行インデックス:  <br/> |**visRow1stHyperlink** +  *i* 、 *i* = 0, 1, 2.  <br/> |
|セル インデックス:  <br/> |**visHLinkDefault** <br/> |
   

