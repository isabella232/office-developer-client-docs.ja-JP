---
title: '[EnableLineProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251696
localization_priority: Normal
ms.assetid: 9f619416-36ff-1479-6232-225c11827e01
description: スタイルに線のプロパティを含めるかどうかを指定します。
ms.openlocfilehash: 38964194626be052b2a168fa929b69ebe4b28e01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329107"
---
# <a name="enablelineprops-cell-style-properties-section"></a>[EnableLineProps] セル ([Style Properties] セクション)

スタイルに線のプロパティを含めるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |線のプロパティを含めます。  <br/> |
|FALSE  <br/> |線のプロパティを含めません。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableLineProps] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[enablelineprops]  <br/> |
   
プログラムから、インデックスによって [EnableLineProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowStyle** <br/> |
|セル インデックス:  <br/> |**visStyleIncludesLine** <br/> |
   

