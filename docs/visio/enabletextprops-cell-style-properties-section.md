---
title: '[EnableTextProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251697
ms.localizationpriority: medium
ms.assetid: 8c59abaf-d2cc-94c9-08ba-004bc40efd9e
description: スタイルにテキストのプロパティを含めるかどうかを指定します。
ms.openlocfilehash: 34b1cf25667ba6fd4354ec2bc6ca3afd5b49bf91
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570646"
---
# <a name="enabletextprops-cell-style-properties-section"></a>[EnableTextProps] セル ([Style Properties] セクション)

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
   

