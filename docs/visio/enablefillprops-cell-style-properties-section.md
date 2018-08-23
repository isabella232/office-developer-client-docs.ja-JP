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
ms.openlocfilehash: 399af4b9d1a2245ea7a9b91ebbf036eb122f15bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19805312"
---
# <a name="enablefillprops-cell-style-properties-section"></a>[EnableFillProps] セル ([スタイルのプロパティ] セクション)

スタイルに塗りつぶしのプロパティを含めるかどうかを指定します。
  
|**値**|**説明**|
|:-----|:-----|
|TRUE  <br/> |塗りつぶしのプロパティを含めます。  <br/> |
|FALSE  <br/> |塗りつぶしのプロパティを含めません。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [EnableFillProps] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
|セル名 :  <br/> |EnableFillProps  <br/> |
   
プログラムから、インデックスによって [EnableFillProps] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
|セクション インデックス:  <br/> |**visSectionObject** <br/> |
|行インデックス:  <br/> |**visRowStyle** <br/> |
|セル インデックス:  <br/> |**visStyleIncludesFill** <br/> |
   

