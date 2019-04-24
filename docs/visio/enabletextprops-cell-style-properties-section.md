---
title: '[EnableTextProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
localization_priority: Normal
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: スタイルにテキストのプロパティを含めるかどうかを指定します。
ms.openlocfilehash: 3f1d87316955b4e6e40cea16634cff7645a720fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328918"
---
# <a name="enabletextprops-cell-style-properties-section"></a>[EnableTextProps] セル ([Style Properties] セクション)

スタイルにテキストのプロパティを含めるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストのプロパティを含めます。  <br/> |
|FALSE  <br/> |テキストのプロパティを含めません。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableTextProps] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[enabletextprops]  <br/> |
   
プログラムから、インデックスによって [EnableTextProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowStyle** <br/> |
|セル インデックス:  <br/> |**visStyleIncludesText** <br/> |
   

