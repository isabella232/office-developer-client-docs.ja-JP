---
title: '[QuickStyleFontColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: 図形のテキストが 0-1 整数値で、作業中のテーマから継承したクイック スタイルからフォントの色を決定します。
ms.openlocfilehash: 8f2d77508dccffccf472f8ab80517e840f860541
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806132"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>[QuickStyleFontColor] セル ([クイック スタイル] セクション)

図形のテキストが 0-1 整数値で、作業中のテーマから継承したクイック スタイルからフォントの色を決定します。 
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形のテキストは [ダーク] のフォントの色を使用します。  <br/> |
|1  <br/> |図形のテキストは [ライト] のフォントの色を使用します。  <br/> |
   
## <a name="remarks"></a>Remarks

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**QuickStyleFontColor**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleFontColor  <br/> |
   
プログラムから、インデックスによって [**QuickStyleFontColor**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleFontColor** <br/> |
   

