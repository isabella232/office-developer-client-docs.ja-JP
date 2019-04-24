---
title: '[EnableFillProps] セル ([Style Properties] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm300
localization_priority: Normal
ms.assetid: 2b3334de-588c-6cf3-bc88-be03ae71b1a6
description: スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。
ms.openlocfilehash: 55191cb28d5777f7fb65a3a1e4be890e6dda4e8b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345564"
---
# <a name="enablefillprops-cell-style-properties-section"></a>[EnableFillProps] セル ([Style Properties] セクション)

スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |塗りつぶしのプロパティを含めます。  <br/> |
|FALSE  <br/> |塗りつぶしのプロパティを含めません。  <br/> |
   
## <a name="remarks"></a>解説

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableFillProps] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |[enablefillprops]  <br/> |
   
プログラムから、インデックスによって [EnableFillProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowStyle** <br/> |
|セル インデックス:  <br/> |**visStyleIncludesFill** <br/> |
   

