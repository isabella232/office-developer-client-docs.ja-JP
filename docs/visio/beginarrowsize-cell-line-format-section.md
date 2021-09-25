---
title: '[BeginArrowSiz] セル ([Line Format] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251629
ms.localizationpriority: medium
ms.assetid: bfddb829-6e13-7d74-b9b9-2cb5c0937bae
description: 線の開始位置にある矢印のサイズを指定します。
ms.openlocfilehash: ed1db98de60368f2c08d8c5e61c1185cce016be2
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628844"
---
# <a name="beginarrowsize-cell-line-format-section"></a>[BeginArrowSiz] セル ([Line Format] セクション)

線の開始位置にある矢印のサイズを指定します。
  
|**値**|**サイズ**|**オートメーション定数**|
|:-----|:-----|:-----|
| 0  <br/> | 極小  <br/> |**visArrowSizeVerySmall** <br/> |
| 1  <br/> | 小  <br/> |**visArrowSizeSmall** <br/> |
| 2  <br/> | 中  <br/> |**visArrowSizeMedium** <br/> |
| 3  <br/> | 大  <br/> |**visArrowSizeLarge** <br/> |
| 4   <br/> | 特大  <br/> |**visArrowSizeVeryLarge** <br/> |
| 5  <br/> | ジャンボ  <br/> |**visArrowSizeJumbo** <br/> |
| 6   <br/> | Colossal  <br/> |**visArrowSizeColossal** <br/> |
   
## <a name="remarks"></a>注釈

矢印のサイズは [**線**] ダイアログ ボックスでも設定できます。 
  
別の数式または **CellsU** プロパティを使用したプログラムから、名前によって [BeginArrowSize] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名 :  <br/> | BeginArrowSize  <br/> |
   
プログラムから、インデックスによって [BeginArrowSize] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowLine** <br/> |
| セル インデックス:  <br/> |**visLineBeginArrowSize** <br/> |
   

