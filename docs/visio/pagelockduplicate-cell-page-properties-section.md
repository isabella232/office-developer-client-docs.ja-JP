---
title: '[PageLockDuplicate] セル ([ページのプロパティ] セクション)'
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fbaa7d64-06ef-46d6-81d5-9d7af1c14b65
description: ページを複製できるかどうかを、ブール演算型で決定します。
ms.openlocfilehash: 8ce730fcdc2dff5deac44d8c053b84e82a82d4cb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ja-JP
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425982"
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
   

