---
title: '[QuickStyleFontColor] セル ([クイック スタイル] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 31c56d08-19ea-4b8b-8be7-42e1c736fbca
description: 図形のテキストがアクティブなテーマから継承するクイック スタイルのフォントの色を、0 から 1 の整数で指定します。
ms.openlocfilehash: 101b7b3b7d534be2ac39a782d2667b2a624b3261
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573608"
---
# <a name="quickstylefontcolor-cell-quick-style-section"></a>[QuickStyleFontColor] セル ([クイック スタイル] セクション)

図形のテキストがアクティブなテーマから継承するクイック スタイルのフォントの色を、0 から 1 の整数で指定します。 
  
|||
|:-----|:-----|
|値  <br/> |説明  <br/> |
|0  <br/> |図形のテキストは [ダーク] のフォントの色を使用します。  <br/> |
|1  <br/> |図形のテキストは [ライト] のフォントの色を使用します。  <br/> |
   
## <a name="remarks"></a>注釈

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
   

