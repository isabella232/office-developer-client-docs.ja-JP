---
title: '[PageLockDuplicate] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: ページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 41ac55f68993f164ae7e31aad0aab4720d58643e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 09/24/2021
ms.locfileid: "59562938"
---
# <a name="pagelockduplicate-cell-page-properties-section"></a>[PageLockDuplicate] セル ([ページのプロパティ] セクション)

ページを複製できるかどうかを、ブール演算型で決定します。
  
|||
|:-----|:-----|
|TRUE  <br/> |このページでは、ページのショートカット メニューの [**複製**] と、**Page.Duplicate** オートメーション メソッドはどちらも無効化されています。  <br/> |
|FALSE  <br/> |このページは複製できます。  <br/> |
   
## <a name="remarks"></a>注釈

別の数式から、**Cell** エレメントの **N** 属性の値によって、または **CellsU** プロパティを使用したプログラムから、名前によって [**PageLockDuplicate**] セルへの参照を取得するには、次の値を使用します。 
  
|||
|:-----|:-----|
| セル名:  <br/> | PageLockDuplicate  <br/> |
   
プログラムから、インデックスによって [**PageLockDuplicate**] セルへの参照を取得するには、**CellsSRC** プロパティを使用し、次の引数を指定します。 
  
|||
|:-----|:-----|
| セクション インデックス:  <br/> |**visSectionObject** <br/> |
| 行インデックス:  <br/> |**visRowPage** <br/> |
| セル インデックス:  <br/> |**visPageLockDuplicate** <br/> |
   

