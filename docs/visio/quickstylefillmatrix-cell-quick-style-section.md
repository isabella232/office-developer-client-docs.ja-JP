---
title: '[QuickStyleFillMatrix] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8513cf3f-42bd-4e76-bfa8-8bf12f0d1296
description: 使用中のテーマから図形を継承したスタイルをクイックスタイルで塗りつぶすかどうかを、0 から 6 の整数で決定します。
ms.openlocfilehash: b3e5d8dc4346b6f5d8f73b220f77978a21a680c4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 06/11/2018
ms.locfileid: "19806133"
---
# <a name="quickstylefillmatrix-cell-quick-style-section"></a>[QuickStyleFillMatrix] セル ([クイック スタイル] セクション)

使用中のテーマから図形を継承したスタイルをクイックスタイルで塗りつぶすかどうかを、0 から 6 の整数で決定します。 
  
## <a name="remarks"></a>Remarks

**セル**要素の**N**属性の値によって、別の数式または**CellsU**プロパティを使用したプログラムから、名前によって、[ **QuickStyleFillMatrix** ] セルへの参照を取得、次のように使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | QuickStyleFillMatrix  <br/> |
   
プログラムから、インデックスによって [ **QuickStyleFillMatrix** ] セルへの参照を取得するのには、次の引数を持つ**CellsSRC**プロパティを使用します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowQuickStyleProperties** <br/> |
| セル インデックス:  <br/> |**visQuickStyleFillMatrix** <br/> |
   

