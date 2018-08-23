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
ms.openlocfilehash: a51f83624192615e84292129d4788ae1e2779c6a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805306"
---
# <a name="enabletextprops-cell-style-properties-section"></a>[EnableTextProps] セル ([スタイルのプロパティ] セクション)

スタイルにテキストのプロパティを含めるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |テキストのプロパティを含めます。  <br/> |
|FALSE  <br/> |テキストのプロパティを含めません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableTextProps] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |EnableTextProps  <br/> |
   
プログラムから、インデックスによって [EnableTextProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowStyle** <br/> |
|セル インデックス:  <br/> |**visStyleIncludesText** <br/> |
   

